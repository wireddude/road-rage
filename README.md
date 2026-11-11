# Road Rage

A 3D endless highway game for desktop, iPhone, and iPad. Eight lanes each way, traffic that bunches and changes speed by lane, near-miss taunts, and arcade shootouts. Keyboard: arrows or WASD to drive, Space or click to fire, R to restart, Esc to pause. Touch devices get on-screen steer, gas, brake, and fire.

Sound is synthesized in the page: a gunshot for the player and a duller one for hostile drivers, an engine that revs with the gas and speed, and a brake squeal while braking. The SOUND button mutes and the choice is remembered. Nothing plays on the title screen; pause and a crash cut the engine.

Recorded driver shouts are not included yet. When the clips are ready, register them and a near-miss taunt will play one:

```js
await __roadRage.audio.addShoutClip('audio/shouts/watch-it.m4a');
await __roadRage.audio.addShoutClip('audio/shouts/asshole.mp3', { name: 'asshole' });
```

`addShoutClip` accepts a URL, an ArrayBuffer, or an AudioBuffer. Until at least one clip is registered, the taunt stays visual only.

Play: https://wireddude.github.io/road-rage/
