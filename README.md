What's a synth?

Oscillator

Why make a javascript synth?

learn new apis and data structures

enrich understanding of the browser

get creative and weird

framework and ui design

its fun

web audio synth* in 10 lines

```
document.querySelector('#play').addEventListener('click', () => {
  const actx = new (AudioContext || webkitAudioContext)();
  if (!actx) throw 'Browser not supported';
  const osc = actx.createOscillator();

  osc.type = 'sawtooth';
  osc.frequency.value = 440;
  osc.connect(actx.destination);
  osc.start();
  osc.stop(actx.currrentTime + 2);
})

```

web audio api

context = global obejct / factory for all web audio applicaitons


