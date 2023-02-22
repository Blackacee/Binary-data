# Binary-data


function ArrayBufferToBinary(buffer) {
 // Convert an array buffer to a string bit-representation: 0 1 1 0 0 0...
 var dataView = new DataView(buffer);
 var response = "", offset = (8/8);
 for(var i = 0; i < dataView.byteLength; i += offset) {
 response += dataView.getInt8(i).toString(2);
 }
 return response;
}
