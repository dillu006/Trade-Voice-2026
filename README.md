# TradeVoice Live — Upstox

This package is a ready-to-run live market-data dashboard.

What is already done:
- Express backend
- Upstox Analytics Token authentication via environment variable
- Upstox Market Quote V3
- Automatic instrument lookup using Upstox Instrument Search
- NIFTY 50 / BANK NIFTY / INDIA VIX lookup
- NSE stocks: Reliance, TCS, Infosys, HDFC Bank, ICICI Bank, SBI, Tata Motors, Bharti Airtel
- Live refresh every 10 seconds
- Telugu browser voice toggle
- No order placement

## One unavoidable step

Your private Upstox Analytics Token cannot be embedded into a file by ChatGPT because it is a secret credential. Put it into `.env` yourself:

UPSTOX_ACCESS_TOKEN=YOUR_TOKEN

Then:

npm install
npm start

Open:
http://localhost:3000

## Important

Never upload/share your Analytics Token, client secret, PAN/Aadhaar, or KYC documents.

The app uses Upstox's current Full Market Quotes V3 endpoint. Upstox documents up to 500 instruments per request and recommends unique `instrument_key` values. Instrument Search can resolve a small set of symbols without manually maintaining instrument keys.
