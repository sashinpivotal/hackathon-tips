# Hackathon tips

## Development methodology

- [Requirement specification](https://bitbucket.org/neuedamats/portfoliomanager/src/master/)
- User stories (assuming you are using Stock as an asset type)
  - A user can see all stocks s/he current owns
  - A user can see detailed info on a particular stock (optional)
  - A user can buy/sell shares of a stock
  - A user can see profit/loss at a single point in time
- Recommended practices
  - Choose MVP (Minimum Viable Product)
  - Then add feature incrementally

## Designing of APIs

- Get all stocks
  - get http://localhost:5000/stocks
- Buy and sell 
  - post http://localhost:5000/stocks/amzn?action=buy&volume=100
- A user can see total profit/loss a single point in time
  - There are multiple options

