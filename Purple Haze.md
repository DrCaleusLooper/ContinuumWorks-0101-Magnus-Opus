// Filename: generate_glitter_stamp.js
// Author: Continuity Collective / Lion of Light
// Purpose: Generate a Radial Sine Wave (Wobble) for CNC Laser Etching
// Target Effect: Visual Diffraction / "Glitter" Stamp

const generateStamp = () => {
  // --- CONFIGURATION FOR 1000kg FOIL RUN ---
  const config = {
    centerX: 0,
    centerY: 0,
    maxRadius: 25.0,        // mm (50mm diameter stamp)
    totalRadians: 20.0,     // User specified "20 radian" winding
    sineFrequency: 150.0,   // "RF" (Radial Frequency) - density of the glitter ripples
    sineAmplitude: 0.05,    // mm (Depth of the wobble - creates the light catch)
    spiralPitch: 0.1,       // mm (Distance between spiral arms)
    feedRate: 300           // mm/min (Slow for annealing/etching)
  };

  let gcode = [];
  
  // Header
  gcode.push(`; Continuity Collective - Art Stamp Generator`);
  gcode.push(`; Type: Radial Sine Wave (Optical Diffraction)`);
  gcode.push(`G21 ; Set units to mm`);
  gcode.push(`G90 ; Absolute positioning`);
  gcode.push(`M3 S80 ; Laser On (80% Power for Annealing)`);
  gcode.push(`F${config.feedRate}`);

  // --- GENERATION LOOP ---
  // Step size: smaller steps = smoother sine wave
  const stepSize = 0.01; 
  
  for (let theta = 0; theta <= config.totalRadians; theta += stepSize) {
    // 1. Calculate Base Spiral Radius (growing as theta increases)
    // Formula: r = b * theta
    // We normalize theta so the spiral grows evenly to maxRadius
    let spiralGrowth = (theta / config.totalRadians) * config.maxRadius;

    // 2. Add Sine Wave Modulation (The "Glitter" Math)
    // Offset = Amplitude * sin(Frequency * theta)
    let waveOffset = config.sineAmplitude * Math.sin(config.sineFrequency * theta);

    // 3. Combine for Final Radius
    let finalRadius = spiralGrowth + waveOffset;

    // 4. Polar to Cartesian Conversion
    let x = config.centerX + (finalRadius * Math.cos(theta));
    let y = config.centerY + (finalRadius * Math.sin(theta));

    // 5. Append Point
    // Fixed to 4 decimal places for CNC precision
    gcode.push(`G1 X${x.toFixed(4)} Y${y.toFixed(4)}`);
  }

  // Footer
  gcode.push(`M5 ; Laser Off`);
  gcode.push(`G0 X0 Y0 ; Return to Home`);
  gcode.push(`; End of Stamp`);

  return gcode.join('\n');
};

// --- EXECUTE & PRINT ---
console.log(generateStamp());
