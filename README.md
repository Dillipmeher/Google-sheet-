# Google-sheet-
Google sheet code - To block the Adding new Sheet in the Google sheet when you are sharing for update data
function onOpen() {
 
  // create variables to carry the file content 
  var ssfile = SpreadsheetApp.getActiveSpreadsheet();
 
 
  // make sure my importnt sheets are in the begining of my file
  var sheet = ssfile.getSheetByName ("BBQ")
  sheet.activate()
  ssfile.moveActiveSheet(1);
 
 var sheets = ssfile.getSheets();
 
  //delete anyother sheets
  for (var i =1; i < sheets.length ; i++ )
  {
ssfile.deleteSheet(sheets[i])
 
  }
 
} 

