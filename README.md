# simpleTimeline - A jQuery Plugin for Drawing Simple Timelines

**Example Screenshot**
![simpleTimeline Example](https://esciencecenter.github.io/assets/simpleTimeline/screenshots/simpleTimeline-screenshot-en.png)

## Features

* Vertically, the timeline is structured into *layers*. Each layer can hold any number of data items that will be displayed as bars with custom CSS styles. In the screenshot below, A01 and A02 are in the first layer, A05 is in the second layer, and so forth. Logical arrangement of layers and bars has to be defined in a `data` array upon timeline initialization. The actual position of the bars on the screen is calculated automatically based on their provided start and end time points.

* Horizontally, the timeline is structured into consecutively aligned *phases*. A timeline needs to span at least one phase. If it has multiple phases, each phase can have its own scale. You can individually define the share of the horizontal timeline space occupied by each phase, as well as the absolute start and end time values for each phase. For example, the screenshot above has 3 phases. The 1st phase is from 50000 to 30000 BC, spanning 20000 years and occupying 20% of the timeline width, the 2nd phase is from 30000 to 7000 BC, spanning 23000 years and occupying 10% of the timeline width. Its custom CSS style shall indicate that it is just bridging an "empty" timeslot. The third phase is from 7000 BC to 2100 AD, occupying the remaining 70% width with vertical dashed indicators every 1000 years. The indicator intervals can be adjusted along with several other settings in the `options` object provided at timeline initialization.

* simpleTimeline can be drawn into any `div` container. The timeline is automatically redrawn when the container width is changed (e.g. after a browser window resize). It is also possible to allow the user to expand and collapse the timeline container.

* It is possible to attach descriptive HTML text to data items. This text is shown in a popup window when the user clicks the respective timeline bar.

* Timeline data can be modified at runtime. This includes adding, removing or updating data items.

## Events

* `timeline:barclick` is triggered when one of the time bars is clicked. As an additional argument, the original jQuery event is passed to the event handler

* `timeline:popup-open` is triggered after a popup window was opened. As additional arguments, the original jQuery event, the popup jQuery object, and the timeline bar jQuery object are passed to the event handler

* `timeline:popup-closing` is triggered immediately before the open popup window is about to be closed. As additional arguments, the popup jQuery object and the timeline bar jQuery object are passed to the event handler

* `timeline:popup-closed` is triggered immediately after a popup window was closed. As an additional argument, the timeline bar jQuery object is passed to the event handler

## Usage Notes

See the [live demo](https://esciencecenter.github.io/simpleTimeline/example.html) source code to see how it works.

The [simpleTimeline.js](simpleTimeline.js) file includes information on how to the `options` and `data` objects are to be used.

simpleTimeline was developed using jQuery v1.12.4.

## License

simpleTimeline is licensed under the MIT License; see the [LICENSE](LICENSE.md) file.
