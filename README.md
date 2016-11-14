# simpleTimeline - A jQuery Plugin for Drawing Simple Timelines

The simpleTimeline can be drawn into any div container. 

Vertically, the timeline is structured into *layers*. Each layer can hold any number of data items that will be displayed as bars with custom CSS styles. In the screenshot below, A01 and A02 are in the first layer, A05 is in the second layer, and so forth. Logical arrangement of layers and bars has to be defined in a `data` array upon timeline initialization. The actual position of the bars on the screen is calculated automatically based on their provided start and end time points.

Horizontally, the timeline is structured into consecutively aligned *phases*. A timeline needs to span at least one phase. If it has multiple phases, each phase can have its own scale. You can individually define the share of the horizontal timeline space occupied by each phase, as well as the absolute start and end time values for each phase. For example, the screenshot below has 3 phases. The 1st phase is from 50000 to 30000 BC, spanning 20000 years and occupying 20% of the timeline width, the 2nd phase is from 30000 to 7000 BC, spanning 23000 years and occupying 10% of the timeline width. Its custom CSS style shall indicate that it is just bridging an "empty" timeslot. The third phase is from 7000 BC to 2100 AD, occupying the remaining 70% width with vertical dashed indicators every 1000 years. The indicator intervals can be adjusted along with several other settings in the `options` object provided at timeline initialization.

The timeline is automatically redrawn when the container width is changed (e.g. after a browser window resize). The timeline object triggers a `timeline:barclick` event when one of the time bars is clicked.

**Example Screenshot**

![simpleTimeline Example](https://esciencecenter.github.io/assets/simpleTimeline/screenshots/simpleTimeline-screenshot-en.png)

## Usage Notes

See the [live demo](https://esciencecenter.github.io/simpleTimeline/example.html) source code to see how it works.

The [simpleTimeline.js](simpleTimeline.js) file includes information on how to the `options` and `data` objects are to be used.

simpleTimeline was developed using jQuery v1.12.4.

