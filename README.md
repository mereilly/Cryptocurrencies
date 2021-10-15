# Cryptocurrencies

The unsupervised learning algorithms give us a wide toolkit to be able to detect patterns from data that is not requiring/seeking a specific target on which to categorize/consider the analysis of the imputs from the dataset. Here, we evaluated various cryptocurrency exchanges, looking for any patterns in the data.


## Note on visualizations
Similar visualizations can be made, but the finer details of which version to pick depends on what you want to convey and emphasize in the graph

Consider the following three, which in theory represent the exact same thing: Total Coins Mined v TotalCoinSupply by class. Which graph would you choose: A, B, or C?

A. (Using scatter_fig = px.scatter(plot_df,
                         x='TotalCoinsMined',
                         y='TotalCoinSupply',
                         color='Class',
                         symbol='Class',
                         width=800,
                         hover_name="CoinName"
                        )
scatter_fig.show()
![Screen Shot 2021-10-15 at 7 02 23 PM](https://user-images.githubusercontent.com/82982952/137562919-1e092059-4dd3-4d52-9e7e-2e9469f33c33.png)

B. (after removing color='Class') Colors can be distracting, unless the colors themselves demonstrate an important patern of growing density, an exception for the audience to focus on, or (which was in our case) separate classes represented on one graph that are being compared, but need to be considered separately. Because of my last point, this graph may not be where we want to apply the monochrome standard, but still something about the way it was color coded was a bit distracting.  
![Screen Shot 2021-10-15 at 7 03 08 PM](https://user-images.githubusercontent.com/82982952/137562945-d3948f63-f99e-4a40-8a3b-e322ba53cb21.png)

C. (using plot_df.hvplot.scatter(x = 'TotalCoinsMined', y = 'TotalCoinSupply', by = 'Class', hover_cols = ['CoinName'])) This was written in one line of code, which is cool on the back end, but practicall speaking what is different here? This is probably the strongest graph because it gives us a legend the separated the different classes without distracting audiences with a gradient like A. We could scale it better and make this graph even stronger, too.
![Screen Shot 2021-10-15 at 7 02 08 PM](https://user-images.githubusercontent.com/82982952/137562905-0aaed4ec-c5dd-4dad-a99a-dd3a282d3422.png)


We also did a 3D graph on the PCAs, but I would take the notes from above seriously in this instance too in determining it's usefulness for this project beyond it looking SO cool:
![Screen Shot 2021-10-15 at 7 14 43 PM](https://user-images.githubusercontent.com/82982952/137563469-c025ed86-be11-43ab-8d75-0fc483649462.png)
