# week8_capstone_project

import holoviews as hv
def load_symbol(variable='adj_close', **kwargs):
    df_2 = forest_area1.loc[['United States', 'Brazil', 'Estonia']].copy()
    forest_combined_plt = df_2.hvplot.bar(x= 'index', groupby= 'Country Name').opts(title= "Forest area USA, Brazil, Estonia")
    df = pd.DataFrame(getattr(stocks, symbol))
    df['date'] = df.date.astype('datetime64[ns]')
    return hv.Curve(forest_combined_plt, ('date', 'Date'), variable).opts(framewise=True)

stock_symbols = ['AAPL', 'IBM', 'FB', 'GOOG', 'MSFT']
dmap = hv.DynamicMap(load_symbol, kdims='Symbol').redim.values(Symbol=stock_symbols)

dmap.opts(framewise=True)