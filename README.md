
# BouncingTextApplet

A simple Java Applet demonstrating basic animation by moving text horizontally across the screen. This project uses deprecated Java Applet APIs and illustrates how to create an animated effect using a separate thread.

---

## Project Overview

This applet displays a custom text string that moves (bounces) from left to right across the applet window. When the text reaches the right edge, it resets to the left side and continues moving.

---

## Features

- Animated text movement controlled by a dedicated animation thread.
- Text resets position after reaching the window’s right edge.
- Customizable display text (currently set to `"My Name (Software Archaeologist)"`).
- Uses basic Java AWT classes (`Applet`, `Graphics`, `Color`, `Font`).
- Simple thread management for starting, running, and stopping animation.
- Sets a dark background with white text for good contrast.

---

## How It Works

- **Initialization (`init`)**: Sets the applet size, background color, font, and vertical position for the text.
- **Animation Thread (`run`)**: Updates the horizontal position (`xCoordinate`) of the text every 100 milliseconds, then requests a repaint.
- **Drawing (`paint`)**: Draws the text at the current x-coordinate and fixed vertical position.
- **Thread Control (`start` and `stop`)**: Starts and stops the animation thread when the applet loads or unloads.

---

## Usage

To run this applet:

1. Use an applet viewer or an IDE that supports Java applets (e.g., older versions of Eclipse or NetBeans).
2. Compile the `BouncingTextApplet.java` file.
3. Load it into an HTML page with the appropriate `<applet>` tag or run it with an applet viewer.
4. The text will move smoothly from left to right, resetting once it moves off-screen.

---

## Important Notes

- **Deprecated Technology**: Java Applets are deprecated and no longer supported by most modern browsers. This example is for educational and legacy purposes only.
- **Animation Reset**: The text resets position to the left once it reaches the right edge, rather than bouncing back.
- **Thread Handling**: Basic thread start/stop logic implemented. In modern Java, other animation frameworks or UI toolkits like JavaFX are recommended.
- **Customization**: Change the `textToDisplay` variable in the code to display your own message.

---

## References

- Uses `java.applet.Applet` and AWT classes for GUI and graphics.
- Implements the `Runnable` interface to handle animation in a separate thread.
- Employs basic synchronization by checking thread identity to stop gracefully.

---

## License

This code is provided for learning and demonstration purposes.

---

Feel free to modify the text or animation speed by adjusting `textToDisplay` and `xSpeed` respectively.
