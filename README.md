[![bitHound Overall Score](https://www.bithound.io/github/NodeArt/EventEmitter/badges/score.svg)](https://www.bithound.io/github/NodeArt/EventEmitter)
[![bitHound Dependencies](https://www.bithound.io/github/NodeArt/EventEmitter/badges/dependencies.svg)](https://www.bithound.io/github/NodeArt/EventEmitter/master/dependencies/npm)
[![bitHound Code](https://www.bithound.io/github/NodeArt/EventEmitter/badges/code.svg)](https://www.bithound.io/github/NodeArt/EventEmitter)

Methods:
```javascript
const EventEmitter = require('@nodeart/event_emitter');
const events = new EventEmitter();
events.on('eventName', ...fns)
      .once('eventName', ...fns)
      .off('eventName', ...fns)
      .emit('eventName', {
          ctx: true
      }, ...args)
      .times('eventName2', 3, ...fns)
      .offAll();

const inherited = {};

// reset prototype
EventEmitter
    .inherit(inherited)
    .on('smth', ...fns);
    
const extended = {};

// add EventEmitter functionality as mixin
EventEmitter
    .extend(extended)
    .on('smth', ...fns);

// One can remove some functions from listeners array by passing them to .off method,
// but to remove all listeners event use .off with eventName only;
```
