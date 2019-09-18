# seal-potato-book

1. The seal and the potato. The beginning of a beautiful friendship.

2. The great divide. When natural disasters cause a problem

3. Reunion. Seal and potato find eachother again

4. Serenity. They move in together and start a bar.

```javascript
import {LifeConstants, IdeaFailedError} from life.js;

let doMoveIn = seal.willMoveInWith(potato);

console.assert(doMoveIn);
if(!doMoveIn) throw new Error("Read the book!");

let union = {'partner0': seal, 'partner1': potato};

let barIdea = union.haveIdea(LifeConstants.Ideas.START_BAR);

let attempts = 0;
let bar;
while(true) {
  try {
    attempts++;
    bar = barIdea.fullfill();
    break;
  } catch (IdeaFailedError e) {
    console.log("Try, try again.");
  } finally {
    console.log("Attempt #" + attempts);
  }
}

union.moveInto(bar.upstairs);
union.happilyEverAfter();
```
