## Generate dynamic excalidraw files

Create flowcharts or any type of chart dynamically with constructing excalidraw json object.

This example
1. generates a few flows, a few objects with different customization options
2. uses https://kroki.io/ to render SVG rendered version of the excalidraw document (encode JSON object, compress and send to kroki API as a simple GET parameter)

Generated excalidraw file can be also downloaded.

### Known issues:

- Text positioning inside rectangles are not automatically calculated by excalidraw, instead we have to position text with its starting position, height, font-size, baseline and all the parameters determine the perfect positioning of a text. Since this is not an official way or how the dynamic text height and position gets calculated (it's probably easy to read from the excalidraw source). For now a rough positioning is done and once you open the file in excalidraw, rect texts may not be cutting on the edges and/or its positions may not be perfect. Just double click to rects and exit the edit mode. Excalidraw will re-render with its correct positioning.