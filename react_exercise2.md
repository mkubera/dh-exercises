# REACT exercise :: Animal in the Forest v2.0

## Description
_Send your forest Animal on a Journey to different lands and see what item it brings back. Count the number of journeys._

## With
- Your app `REACT exercise :: Animal in the Forest`.
- And this data structure
    ```js
    // Animal
    {
      id: String,
      type: String | null,
      journeys: {
        desert: {
          no: Number,
        },
        lake: {
          no: Number,
        }
      },
      items: Array Item
      isHere: Bool,
    }

    // Place
    {
      id: String,
      name: PlaceName,
      items: Array Item,
      image: String,
    }

    // Item
    {
      id: String,
      name: String,
    }

    // PlaceName
    "Desert" | "Lake"
    ```

## Do
1. **FIRST**, create the UI with following elements: 
    - `<select>` or `<input type="radio">` displaying all places (underneath the `Go on a Journey` button)
    - display Animal's Items and detailed info about its Journeys (next to all other information about the Animal)
1. **THEN**, write the application's logic:
    - the Animal can Journey to only one Place at a time
    - when the user sends the Animal on a Journey, increment the correct Journey's `no` by 1
    - when the user summons the Animal back from the Journey, give it an Item from the Items of the Place
      - the Animal can have infinite amount of Items
      - every Place starts with 3 Items
      - the Animal takes a randomly chosen Item from the array of the Place's Items
        - the Item must be deleted from the collection of Place's Items, and added to the collection of Animal's Items


## Use
- `nanoid` npm package for all `ids`
- spread operator and Array methods (`map/filter/etc`) to do CRUD operations on Items
- don't mutate the data( !)
- _(OPTIONAL)_ `TypeScript`


## Notes
You can keep the entire App in a single Functional Component.
