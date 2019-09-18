# seal-potato-book

1. The Seal and the Potato: The beginning of a beautiful friendship.

2. The Great Divide: When natural disasters cause a problem.

3. Reunion: Seal and potato find eachother again.

4. Serenity: Seal and Potato move in together and start a bar.

```javascript
import {LifeConstants, IdeaFailedError} from life.js;

// some small happiness is deserving
let doMoveIn = seal.willMoveInWith(potato);

console.assert(doMoveIn);
if(!doMoveIn) throw new Error("Read the book!"); /* should never happen */

let union = {'partner0': seal, 'partner1': potato};

// the after-story begins
let barIdea = union.haveIdea(LifeConstants.Ideas.START_BAR);

let attempts = 0;
let bar;

// as long as it takes....
do {
  try {
    attempts++;
    bar = barIdea.fullfill();
    // ....they will succeed!
    break;
  } catch (IdeaFailedError e) {
    console.log("Try, try again.");
  } finally {
    console.log("Attempt #" + attempts);
  }
} while(true);

union.moveInto(bar.upstairs.address);
union.happilyEverAfter();

/*********** THE END *************/
```
