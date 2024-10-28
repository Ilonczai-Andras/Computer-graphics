## Course Information
- **Course Codes**: INBMM0635, ILBMM0635L, ILBMB0635L
- **University**: University of Debrecen
- **Course**: Computer Graphics

# Computer Graphics Project 1 - Bouncing Circle

## Required Features (6 Points)
The program must implement the following features to be eligible for a passing grade:

1. **Window Setup**:  
   - Create a 600x600 pixel window with a yellow background (shade of yellow is customizable).

2. **Circle Rendering**:
   - Render a circle of radius `r = 50` centered in the window with a green outline, a red center, and linearly interpolated colors between them.
   - Pass the circle's center coordinates to the fragment shader as a uniform variable (initial colors for green and red are customizable).

3. **Horizontal Movement**:
   - The circle should start at the center of the window and move horizontally along the x-axis.
   - The circle must bounce off the window edges accurately when it touches them.

4. **Horizontal Line**:
   - Draw a horizontal line in the center of the screen with a length of one-third of the window width, a thickness of 3 pixels, and a blue color.

## Optional Enhancements (Bonus Points)
To earn additional points, consider implementing any of the following features:

- **User Interaction (3 Points)**:
  - Allow users to move the horizontal line up and down using the up and down arrow keys.

- **Dynamic Color Change (3 Points)**:
  - When the circle is no longer intersecting with the horizontal line, swap the colors of the circle’s green outline and red center. This should impact the interpolated inner colors of the circle.

- **Angle-Based Movement (3 Points)**:
  - Add a 10-pixel directional vector based on an angle `0° < α < 90°` and use it to start the circle’s movement when the **`s(tart)`** key is pressed. The circle should bounce off the screen edges at the correct angle upon impact.

# Computer Graphics Project 2 - Bézier Curve Drawing Application

## Required Features (6 Points)
To achieve a passing grade, the following features must be implemented:

1. **Third-Degree Bézier Curve**:
   - Use a sample program function to draw a third-degree Bézier curve with a broken line using 4 control points.

2. **Control Point Rendering**:
   - Render up to 4 round control points (with a degree between 3 and 9).

3. **Drag-and-Drop Functionality**:
   - Implement drag-and-drop functionality for control points.
   - The curve should update in real-time as the control points are moved, ensuring detail in the broken line representation.

## Optional Enhancements (Bonus Points)
Additional features can be implemented for bonus points, as follows:

- **Control Polygon (3 Points)**:
  - Draw the control polygon that connects the control points, enhancing the curve's visual representation.

- **Color Customization (3 Points)**:
  - Use three distinct colors for the Bézier curve, control points, and control polygon, allowing for a more visually intuitive interface.

- **Dynamic Control Point Addition/Removal (3 Points)**:
  - Add a new control point at the clicked position with a left-click on an empty area.
  - Remove a control point by right-clicking on an existing point.
  - Recalculate and redraw the Bézier curve based on the updated control points.

 # Computer Graphics Project 3 - 3D Cube Scene with Camera and Lighting

## Required Features (6 Points)
The following features are necessary to meet the minimum requirements for a passing grade:

1. **Camera Setup**:
   - **Initial Position**: The camera starts at `(r, 0, 0)` where `8 ≤ r ≤ 10`.
   - **Orientation**:
     - **UP Vector**: Set to `(0, 0, 1)`.
     - **View Direction**: The camera should always look at the origin.
   - **Movement**:
     - Rotate the camera around the `z-axis` along a circular path of radius `r` using the left and right arrow keys.
     - Move the camera up and down along the `z-axis` with the up and down arrow keys.
   - **Projection**: Use a perspective projection with a 55-degree field of view.

2. **Scene with Cubes**:
   - Include three unit cubes:
     - The first cube is centered at the origin.
     - Position the other two cubes above and below the central cube in the camera’s view.
   - All cubes should be equally spaced and sized, with enough space to fit additional cubes between them.
   - Set the cubes’ color to white.

## Optional Enhancements (Bonus Points)
The program can be extended with additional features to earn bonus points:

- **Dynamic Lighting (3 Points)**:
   - Add a colored diffuse light source that moves around the `z-axis` in a circular path at `z = 0` with a radius of `2 * r`.
   - Render the cubes with proper visibility according to the light source’s position.

- **Light Source Representation (3 Points)**:
   - Represent the light source as a sphere with diameter `dsphere = 0.5`.
   - The sphere’s color should match the light source color and should be displayed without lighting.

- **Shader Customization**:
   - **New Shader Files**:
     - Create two additional shader files to handle the light sphere and the cubes separately.
     - The second vertex shader should perform the usual transformations (model, view, and projection matrices).
     - The new fragment shader should simply assign the light color to the displayed fragments.
   - **Shader Program Management**:
     - Modify the `createShaderProgram` function to support multiple shader files.
     - Ensure to use `glUseProgram` to toggle between shaders as needed.

