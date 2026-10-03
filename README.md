# Physics-Project
# Physics Calculator

An Android app that solves common physics problems and shows the results with graphs. I built it as a first-year Computer Science student for a physics project.

# Features

The app covers these topics:

**Linear Motion (SUVAT)**: displacement, velocity, acceleration, and time
**Projectile Motion**: flight time, maximum height, horizontal range, landing angle
**Circular Motion**: angular speed, centripetal acceleration, centripetal force
**Relative Motion**: motion of two objects and the gap between them
**Simple Harmonic Motion**: pendulum and spring-mass systems
**Waves** and **Standing Waves**: frequency, wavelength, harmonics
**Doppler Effect**
**Power & Sound**: intensity and distance
**Formula Reference**: the formulas behind each calculator

Each calculator takes inputs, computes the result, and plots graphs such as height vs time and displacement vs time.

# How it was built

1. I wrote the physics calculation logic in **C++**.
2. I then converted that logic into a working Android app using **AI tools**.
3. The app is packaged as an **Android APK**.

# Install

1. Download `Physics Calculator app.apk` from this repository.
2. Open it on an Android phone.
3. If asked, allow installing apps from this source.

# Known limitations

This is a small, student-level project. It still has some bugs, because we ran short on time and presented it as it was. I tested the calculation logic afterwards and found the issues below. I plan to fix them.

| # | Calculator | Input | App shows | Should show |
|---|------------|-------|-----------|-------------|
| 1 | Linear Motion | u = 20, a = -9.8, s = 0 | t = 0 s | t = 4.08 s (ball returns to start) |
| 2 | Linear Motion | u = 20, a = -9.8, s = -10 | t = -0.45 s, v = +24.41 | t = 4.53 s, v = -24.41 |
| 3 | Projectile | u = 20, angle = 45, launch height = 10 | Max height = 10.20 m | 20.20 m (the graph already shows this) |
| 4 | Projectile | u = 20, angle = -30, launch height = 10 | Max height = 5.10 m | 10 m (the launch point) |
| 5 | Projectile | u = 20, angle = 90 | Range = 4.999e-15 m | 0 m (rounding error shown) |
| 6 | SHM Spring-Mass | A = 1, x = 2 | KE = -6 J | An error, since x cannot be larger than A |
| 7 | Doppler Effect | source speed = 400 m/s | f = -3008.77 Hz | A warning, since the source is faster than sound |
| 8 | Circular Motion | a_c = 8, w = 2 | Radius not calculated | r = 2 m |
| 9 | Projectile | u = 10, angle = 30, g = 10 (textbook value) | Range = 8.84 m (g is fixed at 9.8, no gravity input) | 8.66 m |

Other general issues:

- When the input is invalid, the app shows "-" and does not explain why.
- The Projectile calculator cannot find the starting speed from a target point, such as a basketball hoop at a given distance and height.
- The Relative Motion calculator handles only two objects on one straight line that meet or overtake each other. It cannot find unknown speeds, the gap after a given time, or perpendicular motion such as a boat crossing a stream.
- Circular Motion does not show the distance travelled in one revolution (the circumference).

I also tested the app's calculation logic on textbook problems from my physics chapter. The results were correct for Projectile Motion (except g = 10), Circular Motion, and the jet example in Relative Motion.


# Screenshots

<img width="720" height="1433" alt="Screenshot_20261003_174952_My Project" src="https://github.com/user-attachments/assets/3622c379-c358-47c7-8901-d786e2ef8e9d" />

<img width="720" height="1479" alt="Screenshot_20261003_174957_My Project" src="https://github.com/user-attachments/assets/517f340c-f5ae-49ef-8aad-d9676fd4b84c" />

<img width="720" height="1478" alt="Screenshot_20261003_175001_My Project" src="https://github.com/user-attachments/assets/cc6c1fc5-2743-4618-a0f4-3b74ac36cbf3" />

<img width="720" height="1455" alt="Screenshot_20261003_175159_My Project" src="https://github.com/user-attachments/assets/a16040fc-f497-4d68-9e0e-795c1e7d1492" />

<img width="720" height="1436" alt="Screenshot_20261003_175202_My Project" src="https://github.com/user-attachments/assets/ba74e807-12c5-4a0e-b4ef-1d8f654d6f6a" />

<img width="720" height="1343" alt="Screenshot_20261003_175209_My Project" src="https://github.com/user-attachments/assets/318ed7e4-f8f8-47f4-8e95-8224fa5460ec" />

# What I learned

- Turning physics formulas into correct, working code
- Handling inputs and checking that results are accurate
- Using AI tools to turn working logic into a finished app, and checking the output myself

# Author

**Hania Nawab**
BS Computer Science, Namal University
