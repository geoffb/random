# @mousepox/random

Deterministic pseudorandom number generator based on a [linear congruential generator](https://en.wikipedia.org/wiki/Linear_congruential_generator) algorithm.

## API Reference

### Random

`Random (seed?: number)`

Example:
```ts
// A new instance with a randomized seed
let random = new Random();

// A new instance with a specific seed
let seeded = new Random(1234567);
```

#### chance

`chance (probability: number): number`

Returns whether or not a random number falls within a given probability.

Example:
```ts
if (random.chance(0.5)) {
	// Chance succeeded, do something
}
```

#### next

`next (): number`

Returns the next random number.

Example:
```ts
let n = random.next();
// n = 0.8264938
```

#### reset

`reset (seed?: number)`

Resets the current state to a specified or randomized value.

Example:
```ts
// Reset to a new randomized value
random.reset();

// Reset to a specific value
random.reset(1234567);
```
