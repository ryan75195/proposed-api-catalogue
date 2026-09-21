# Farm Gate Prices

Small farmers sell at wholesale prices they learn about too late. A weekly price signal helps them decide whether to hold or sell a crop.

Farm Gate Prices returns recent indicative prices for a commodity in a region. A call to GET /prices?commodity=wheat&region=midlands returns { "pencePerKg": 24.5, "trend": "up", "samples": 42 }.

Limits: prices are indicative aggregates of reported trades, not quotes, and lag the market. It is not financial advice and cannot guarantee a sale price.

This is a proposed design and is not implemented.

The trend is a simple comparison of the latest window against the prior one rather than a statistical forecast. Sample counts are returned so users can judge how robust an average is.

A typical caller is a farmer deciding whether to sell now or hold for a better window. The indicative level helps timing but is not a guarantee of the price actually paid.
