# Kaaba Beam

A 3D page that shoots a beam straight up from the Kaaba in Mecca and shows where it points in space as the Earth spins and moves around the Sun.

You can pick other places too (Dhaka, Dubai, Moscow, or any latitude and longitude).

## How to run

No install needed. Open `index.html` in a web browser. You need internet, because the page loads its 3D library from a CDN.

To run it from a local server instead:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## What you can do

- **Earth / Orbit / Kaaba sky**: three ways to look at the scene.
- **Place**: choose a city or type your own latitude and longitude.
- **Year view**: see the beam's path for the whole year, and compare two places.
- **Speed and date**: play, pause, speed up time, or jump to any date.
- **Sizes and orbit shape**: switch between easy-to-see sizes and true sizes.

## What it shows

- The beam goes straight up from the ground, along the ellipsoid normal.
- The Earth spins once every sidereal day (23h 56m), and its axis is tilted 23.44°.
- The Earth moves on its real, slightly oval orbit around the Sun.
- The Moon orbits the Earth and shows the right phase.
- The panel shows where the beam points in the sky (right ascension and declination) and the nearest bright star.

At one clock time, the beam moves about 1° across the sky each day, so over a year it goes once around a full circle.

## The physics used

- Earth orbit: JPL orbital elements for the Earth–Moon centre.
- Earth direction: sidereal time, precession, and a short nutation series.
- Earth shape: WGS84 ellipsoid.
- Moon: a short version of the standard lunar series (about 0.1° accuracy).
- Stars: bright stars at J2000 positions.

Not included: aberration, polar motion, UT1−UTC, deflection of the vertical, and star motion. The beam direction should be good to a few arcseconds.

## Display choices (not to scale)

By default the Earth, Sun and Moon are drawn bigger than real, the Moon is moved closer, and the orbit's oval shape is stretched ×10 so you can see it. Use the buttons to switch to true sizes and the true orbit shape. The Kaaba sky view always uses true sizes.

## Built with

- [three.js](https://threejs.org) for 3D
- Plain HTML, CSS and JavaScript, in one file

## License

MIT
