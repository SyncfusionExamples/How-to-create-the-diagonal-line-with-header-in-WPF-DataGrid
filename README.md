# How to create the diagonal line with header in WPF DataGrid?

In [WPF DataGrid](https://www.syncfusion.com/wpf-controls/datagrid) (SfDataGrid),  a diagonal line can be added to a column header by using the [HeaderTemplate](https://help.syncfusion.com/cr/wpf/Syncfusion.UI.Xaml.Grid.SfDataGrid.html#Syncfusion_UI_Xaml_Grid_SfDataGrid_HeaderTemplate) property. This can be achieved by creating a custom `DataTemplate` and assigning it to the `HeaderTemplate`.
 
 ```xml
 <syncfusion:GridTextColumn HeaderText="Order ID" 
                            MappingName="OrderID">
     <syncfusion:GridTextColumn.HeaderTemplate>
         <DataTemplate>
             <Grid>
                 <Grid.RowDefinitions>
                     <RowDefinition/>
                     <RowDefinition/>
                 </Grid.RowDefinitions>
                 <TextBlock Grid.Row="0" 
                            Text="Value1" 
                            HorizontalAlignment="Center"
                            VerticalAlignment="Center"/>
                 <TextBlock Grid.Row="1" 
                            Text="Value2" 
                            HorizontalAlignment="Center"
                            VerticalAlignment="Center"/>
                 <Line Grid.RowSpan="2" X1="150" Y1="0" X2="0" Y2="90" 
                       Stroke="Black"  
                       StrokeThickness="2"/>
             </Grid>
         </DataTemplate>
     </syncfusion:GridTextColumn.HeaderTemplate>
 </syncfusion:GridTextColumn>

 ```
 
![Diagonal line in Header](DiagonalHeader.png)

Take a moment to peruse the [WPF DataGrid - HeaderTemplate](https://help.syncfusion.com/wpf/datagrid/styles-and-templates#changing-headertemplates) documentation, where you can find about customization of particular column header with code examples.