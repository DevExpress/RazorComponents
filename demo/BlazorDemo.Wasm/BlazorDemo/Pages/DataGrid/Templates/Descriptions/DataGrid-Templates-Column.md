You can use the [DisplayTemplate](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxDataGridColumn.DisplayTemplate) and [EditTemplate](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxDataGridColumn.EditTemplate) properties to specify custom content for the column and its editor. Use the template's **context** parameter to access a data object and its fields.

When you use an edit template, you should call the [CellEditContext.OnChanged](https://docs.devexpress.com/Blazor/DevExpress.Blazor.CellEditContext.OnChanged.overloads) method to inform the Data Grid about changes and save new cell values to the [EditedValues](https://docs.devexpress.com/Blazor/DevExpress.Blazor.CellEditContext.EditedValues) collection. Then, pass this collection to the [RowInserting](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxDataGrid-1.RowInserting) and [RowUpdating](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxDataGrid-1.RowUpdating) events.

This demo customizes the **Details** column. The display template shows the **More Info...** links. Users can click these links to view details about data rows in a pop-up window. The edit template embeds the Memo component into the edit form.