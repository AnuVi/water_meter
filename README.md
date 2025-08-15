# water_meter

<img width="953" height="224" alt="image" src="https://github.com/user-attachments/assets/57a2b759-9fe2-4d42-8d2d-23066b98323c" />
<img width="1684" height="694" alt="image" src="https://github.com/user-attachments/assets/1d2c818a-23fe-4ae4-886f-3c8b222ee8db" />
<img width="1150" height="716" alt="image" src="https://github.com/user-attachments/assets/8ba99e36-7afb-4a9a-a35d-3213a709f7b6" />

<img width="741" height="487" alt="image" src="https://github.com/user-attachments/assets/14b245cb-4814-4356-b458-42612b19307c" />
<img width="999" height="424" alt="image" src="https://github.com/user-attachments/assets/ac1fe800-2fd9-48c0-a559-8e32036c2871" />

<img width="824" height="272" alt="image" src="https://github.com/user-attachments/assets/879fe190-dad6-4b63-9c2f-c48c16cf4fc4" />
function addRowAndDate() {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  
  // Lisa tühi rida enne teist rida (esimene andmerida) - Add empty row after the first row - because it's headline-row
  sheet.insertRowBefore(2);

  // Kuupäev - Day
  const today = new Date();
  const firstDayOfMonth = new Date(today.getFullYear(), today.getMonth(), 1);

  // Vorminda kuupäev kujule "dd.mm.yyyy" - European date-format
  const day = ("0" + firstDayOfMonth.getDate()).slice(-2);
  const month = ("0" + (firstDayOfMonth.getMonth() + 1)).slice(-2);
  const year = firstDayOfMonth.getFullYear();
  const formattedDate = `${day}.${month}.${year}`;

  // Pane see kuupäev lahtrisse A2 (sest uus rida lisati rea 2 ette) - add date to cell A2
  sheet.getRange("A2").setValue(formattedDate);
}


//
function addRowAndDate() {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  
  // Lisa tühi rida enne teist rida (esimene andmerida)
  // Insert a blank row before row 2 (the first data row)
  sheet.insertRowBefore(2);

  // Kuupäev - kuu esimene päev
  // Date - first day of the current month
  const today = new Date();
  const firstDayOfMonth = new Date(today.getFullYear(), today.getMonth(), 1);

  // Vorminda kuupäev kujule "dd.mm.yyyy"
  // Format the date as "dd.mm.yyyy"
  const day = ("0" + firstDayOfMonth.getDate()).slice(-2);
  const month = ("0" + (firstDayOfMonth.getMonth() + 1)).slice(-2);
  const year = firstDayOfMonth.getFullYear();
  const formattedDate = `${day}.${month}.${year}`;

  // Pane see kuupäev lahtrisse A2 (sest uus rida lisati rea 2 ette)
  // Put this date into cell A2 (since a new row was inserted before row 2)
  sheet.getRange("A2").setValue(formattedDate);

  // Võta andmed eelmise rea C3 lahtrist
  // Get data from previous row's C3 cell
  const previousDataC = sheet.getRange("C3").getValue();

  // Pane need andmed lahtrisse B2
  // Put that data into cell B2
  sheet.getRange("B2").setValue(previousDataC);

  // Võta andmed eelmise rea F3 lahtrist
  // Get data from previous row's F3 cell
  const previousDataF = sheet.getRange("F3").getValue();

  // Pane need andmed lahtrisse E2
  // Put that data into cell E2
  sheet.getRange("E2").setValue(previousDataF);
}
<img width="564" height="226" alt="image" src="https://github.com/user-attachments/assets/ae9d114b-f00a-43ba-ab55-8cb9de9377d3" />

function addRowAndDate() {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  
  // Lisa tühi rida enne teist rida (esimene andmerida)
  // Insert a blank row before row 2 (the first data row)
  sheet.insertRowBefore(2);

  // Kuupäev - kuu esimene päev
  // Date - first day of the current month
  const today = new Date();
  const firstDayOfMonth = new Date(today.getFullYear(), today.getMonth(), 1);

  // Vorminda kuupäev kujule "dd.mm.yyyy"
  // Format the date as "dd.mm.yyyy"
  const day = ("0" + firstDayOfMonth.getDate()).slice(-2);
  const month = ("0" + (firstDayOfMonth.getMonth() + 1)).slice(-2);
  const year = firstDayOfMonth.getFullYear();
  const formattedDate = `${day}.${month}.${year}`;

  // Pane see kuupäev lahtrisse A2 (sest uus rida lisati rea 2 ette)
  // Put this date into cell A2 (since a new row was inserted before row 2)
  sheet.getRange("A2").setValue(formattedDate);

  // Võta andmed eelmise rea C3 lahtrist
  // Get data from previous row's C3 cell
  const previousDataC = sheet.getRange("C3").getValue();

  // Pane need andmed lahtrisse B2
  // Put that data into cell B2
  sheet.getRange("B2").setValue(previousDataC);

  // Võta andmed eelmise rea F3 lahtrist
  // Get data from previous row's F3 cell
  const previousDataF = sheet.getRange("F3").getValue();

  // Pane need andmed lahtrisse E2
  // Put that data into cell E2
  sheet.getRange("E2").setValue(previousDataF);

  // Lisa valemid D2 ja G2 lahtritesse
  // Add formulas into cells D2 and G2
  sheet.getRange("D2").setFormula("=C2-B2");
  sheet.getRange("G2").setFormula("=F2-E2");
}

