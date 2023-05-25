---
title: Import Table From Data Table
linktitle: Import Table From Data Table
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/import-table-from-data-table/
---
### Sample source code for Import Table From Data Table using Aspose.Words for .NET 
```csharp
		public Table ImportTableFromDataTable(DocumentBuilder builder, DataTable dataTable,
            bool importColumnHeadings)
        {
            Table table = builder.StartTable();
            // Check if the columns' names from the data source are to be included in a header row.
            if (importColumnHeadings)
            {
                // Store the original values of these properties before changing them.
                bool boldValue = builder.Font.Bold;
                ParagraphAlignment paragraphAlignmentValue = builder.ParagraphFormat.Alignment;
                // Format the heading row with the appropriate properties.
                builder.Font.Bold = true;
                builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
                // Create a new row and insert the name of each column into the first row of the table.
                foreach (DataColumn column in dataTable.Columns)
                {
                    builder.InsertCell();
                    builder.Writeln(column.ColumnName);
                }
                builder.EndRow();
                // Restore the original formatting.
                builder.Font.Bold = boldValue;
                builder.ParagraphFormat.Alignment = paragraphAlignmentValue;
            }
            foreach (DataRow dataRow in dataTable.Rows)
            {
                foreach (object item in dataRow.ItemArray)
                {
                    // Insert a new cell for each object.
                    builder.InsertCell();
                    switch (item.GetType().Name)
                    {
                        case "DateTime":
                            // Define a custom format for dates and times.
                            DateTime dateTime = (DateTime) item;
                            builder.Write(dateTime.ToString("MMMM d, yyyy"));
                            break;
                        default:
                            // By default any other item will be inserted as text.
                            builder.Write(item.ToString());
                            break;
                    }
                }
                // After we insert all the data from the current record, we can end the table row.
                builder.EndRow();
            }
            // We have finished inserting all the data from the DataTable, we can end the table.
            builder.EndTable();
            return table;
        }
```