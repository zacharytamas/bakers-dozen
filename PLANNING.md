# Component Planning

## Data Structures

```typescript
type CardSuite =
  'Hearts' | 'Diamonds' | 'Clubs' | 'Spades';

type CardRank =
  1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 'k' | 'q' | 'j';

interface Card {
  suit: CardSuite
  rank: CardRank
  faceUp: boolean
}

interface Stack {
  cards: Card[]
}

interface BoardState {
  tableauStacks: Stack[]
  foundationStacks: Stack[]
}

interface GameState {
  board: BoardState
}
```

## Visual Components

### `game-card`

This is a playing card. Fortunately this is provided to us by the open source community. Documentation here: [`game-card`](https://www.webcomponents.org/element/vpusher/game-card).

### `card-stack`

This component accepts an array of objects representing a deck of cards and displays them in a stack.

#### Properties

- `stack: Stack`. A `Stack` of `Cards` (described above)

### `tableau-area`

This component accepts an array of `Stack`s and lays them out on the page.

### `foundations-area`

This component accepts an array of `Stack`s representing the foundations stacks and lays them out on the page.

## Logic Components

### `board-generator`

#### Methods

- `generateNewBoardState(): BoardState`. Generates a new state of the board. This means it takes a standard 52 card deck and shuffles them into 13 `Stack`s of four `Card`s and returns it as a `BoardState`.

## Psuedocode for structure

Not actually valid but an example of how these might be composed together.

```html
<bakers-dozen-app game-state="{{gameState}}">
  <game-board state="{{gameState.boardState}}">
    <tableau-area stacks="{{state.tableauStacks}}">
      <template is="dom-repeat" items="[[stacks]]" as="stack">
        <card-stack stack="[[stack]]"></card-stack>
      </template>
    </tableau-area>
    <foundations-area stacks="{{state.foundationsStacks}}">
      <template is="dom-repeat" items="[[stacks]]" as="stack">
        <card-stack stack="[[stack]]"></card-stack>
      </template>
    </foundations-area>
  </game-board>
</bakers-dozen-app>
```