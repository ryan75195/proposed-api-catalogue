# UK Farm Gate Commodity Prices API

I need current prices farmers are paid for wheat, cattle and vegetables in the UK. Small farmers sell at wholesale prices they learn about too late, and a weekly price signal helps them decide whether to hold or sell a crop.

UK Farm Gate Commodity Prices API returns recent indicative prices for a commodity in a region. A call to GET /prices?commodity=wheat&region=midlands returns { "pencePerKg": 24.5, "trend": "up", "samples": 42 }.

Limits: prices are indicative aggregates of reported trades, not quotes, and lag the market. It is not financial advice and cannot guarantee a sale price.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The trend is a simple comparison of the latest window against the prior one rather than a statistical forecast. Sample counts are returned so users can judge how robust an average is.

A typical caller is a farmer deciding whether to sell now or hold for a better window. The indicative level helps timing but is not a guarantee of the price actually paid.
