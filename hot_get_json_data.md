Get the data after serializing it into a JSON, transmit it by attaching it to a hidden input that is part of the submitted form
````
const hot = createHansontable(input_grid, headers, data);
var handsontableData = hot.getData();
var handsontableDataString = JSON.stringify(handsontableData);
document.getElementById('hot-hidden-input').value = handsontableDataString;
````
