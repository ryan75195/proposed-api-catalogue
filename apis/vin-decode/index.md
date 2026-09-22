# VIN Decoder API Return Vehicle Make Model Year API

Developers building vehicle apps (auctions, valuations, insurance) need to send a 17-character VIN and get back make, model, year, engine and dimensions. Existing free services only cover US vehicles, so teams serving other markets cannot rely on them.

VIN Decoder API takes a VIN and returns structured vehicle attributes. A call to GET /vehicles/{vin} returns { "vin": "WVWAA11AA0A1B2C3D", "make": "Volkswagen", "model": "Golf", "year": 2018, "bodyType": "hatchback", "engine": { "capacityCc": 2000, "fuel": "petrol" }, "dimensions": { "lengthMm": 4258, "widthMm": 1727, "heightMm": 1479 } }.

Limits: coverage and field detail vary by market and model year. The NHTSA VPIC API covers US vehicles only and with limited fields; a European requester would reject it for multi-brand data, so results here are not guaranteed for every manufacturer.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The year is the model year, which can differ from the year of first registration. Engine and dimension fields may be absent when the VIN matches no published record for that market.