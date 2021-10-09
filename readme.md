
   ![](./img/2.png)
  </tr>
   <Window.Resources>
        <BitmapImage 
                                   x:Key='defaultImage' 
                                   UriSource='./Images/picture.png' />
    </Window.Resources>

    <Grid 
    Margin="10" 
    HorizontalAlignment="Stretch">

        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="64"/>
            <ColumnDefinition Width="*"/>
            <ColumnDefinition Width="auto"/>
        </Grid.ColumnDefinitions>

  
    <WrapPanel
                Orientation="Horizontal"
                Grid.Column="1"
                MinHeight="50">
                
            </WrapPanel>
        <ListView
    Grid.Row="1"
    Grid.Column="1"
    
    ItemsSource="{Binding ProductList}">
            <ListView.ItemContainerStyle>
                <Style 
            TargetType="ListViewItem">
                    <Setter 
                Property="HorizontalContentAlignment"
                Value="Stretch" />
                </Style>
            </ListView.ItemContainerStyle>
            <ListView.ItemTemplate>
            <DataTemplate>
                <Border 
            BorderThickness="1" 
            BorderBrush="Black" 
            CornerRadius="5">

                        <Grid 
    Margin="10" 
    HorizontalAlignment="Stretch">

                            <Grid.ColumnDefinitions>
                                <ColumnDefinition Width="64"/>
                                <ColumnDefinition Width="*"/>
                                <ColumnDefinition Width="auto"/>
                            </Grid.ColumnDefinitions>

                            <Image
                                Width="64"
                                Height="64"
                                Source="{Binding picture,TargetNullValue={StaticResource defaultImage}}"/>
                            
                            <StackPanel
                                Grid.Column="1"
                                Margin="5"
                                Orientation="Vertical">
                                <TextBlock
                                    Text="{Binding TypeAndName}"/>
                                <TextBlock
                                    Text="{Binding ArticleNumber}"/>
                                <TextBlock
                                    Text="{Binding MaterialString}"/>
                            </StackPanel>

                            <TextBlock   Grid.Column="2"
                                Text="{Binding Total}"/>

                        </Grid>

                    </Border>
            </DataTemplate>
            </ListView.ItemTemplate>
        </ListView>
        




  </Grid>
   </Window>





