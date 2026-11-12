# Road Rage

A 3D endless highway game for desktop, iPhone, and iPad. Eight lanes each way. One marked car is the chase: it runs the fast lanes and shoots back, and traffic jams and gaps are how you catch it. A bump costs health. A hard smash wrecks you. Keyboard: arrows or WASD to drive, Space or click to fire, R to restart, Esc to pause. Touch devices get large steer buttons, plus gas, brake, and fire.

Sound is synthesized in the page: a laser shot for the player and a lower one for hostile drivers, an engine that revs with the gas and speed, a brake squeal while braking, and an impact when the car crashes. The SOUND button mutes and the choice is remembered. Nothing plays on the title screen; pause and a crash cut the engine.

A near-miss taunt plays `audio/shouts/asshole.m4a`. To add another recording, put the file in `audio/shouts/` and add it to `BUNDLED_SHOUTS` in `index.html`, or register it yourself:

```js
await __roadRage.audio.addShoutClip('audio/shouts/watch-it.m4a', { name: 'watch-it' });
```

`addShoutClip` accepts a URL, an ArrayBuffer, or an AudioBuffer. Clips are fetched up front and decoded on the first tap, which is when iOS allows audio.

Play: https://wireddude.github.io/road-rage/
