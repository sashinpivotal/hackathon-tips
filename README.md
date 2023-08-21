# Hackathon tips

## Requirement

- [Requirement specification](https://bitbucket.org/neuedamats/portfoliomanager/src/master/)

## Development methodology

- User stories (assuming you are using Stock as an asset type)
  - A user can see all stocks s/he current owns
  - A user can see detailed info on a particular stock (optional)
  - A user can buy/sell shares of a stock
  - A user can see profit/loss at a single point in time
- Recommended practices
  - Choose MVP (Minimum Viable Product)
    - Choose simplest data model
    - Draw wireframes for UI
    - Abstract needed functionality
      - For example, create "get_current_price(stock)" 
        method and returns some mock value initially
      - Later on, you can replace it with logic
        that gets the real-time value
    - Use simplest UI possible
    - Start something simple
  - Then add feature incrementally

## Designing of REST APIs

- Get all stocks
  - get http://localhost:5000/stocks
- Buy and sell 
  - post http://localhost:5000/stocks/amzn?action=buy&volume=100
- A user can see total profit/loss a single point in time
  - Do you need to create an API for this? 
  - Can profit/loss be displayed automatically 
    when all stocks are displayed?
    - If you take this approach, where do you do
      this computation, client or server?

## UI

- You are welcome to use your own HTML/CSS but
  feel free to use Bootstrap, which is "simpler
  to use" to create a [Grid](https://www.w3schools.com/bootstrap/bootstrap_grid_system.asp)
- Creating graphical chart is nice to have but
  not critical so consider adding chart only 
  when all the other functionality is finished