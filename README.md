

- [Requirement](#requirement)
- [Development methodology](#development-methodology)
- [Database Schema and Object model](#database-schema-and-object-model)
  - [Schema](#schema)
  - [Object model](#object-model)
- [Designing of REST APIs](#designing-of-rest-apis)
- [UI](#ui)
- [GitHub CoPilot](#github-copilot)

## Requirement

- [Requirement specification](https://bitbucket.org/neuedamats/portfoliomanager/src/master/)
- User stories (assuming you are using Stock as an asset type)
  - A user can see all stocks s/he current owns
  - A user can see detailed info on a particular stock 
    (only if there is more detailed info that can be
    displayed in the "display all stocks")
  - A user can buy/sell shares of a stock
  - A user can see profit/loss at a single point in time

## Development methodology
 
- Recommended practices
  - Work on MVP (Minimum Viable Product) 
    - Backend
      - Choose simplest data model
      - Design REST API
      - Abstract needed functionality if needed
        - For example, if there is a need to get current
        price of a stock, you can create "get_current_price(stock)" 
        method and returns some mock "current price" value initially
        - Later on, you can replace it with logic
        that retrieves the real-time stock price value
    - UI    
      - Use simplest UI possible
      - Draw wireframes for UI
    - Start something simple
      - For example, make end-to-end operation work
        for displaying all stocks first 
        (as demonstrated by Lucas during the class)
      - Then add feature incrementally
  - Work in two-hour SPRINT cycles
    - Work on a small feature one at a time that could
      be implemented in ~two-hour cycle

## Database Schema and Object model

### Schema 
- For "stocks" table, what fields do you need?
  - stock symbol
  - volume
  - Do I want profit/loss field in the table
    or can it be computed at the request of
    a user?
  
- What would be the primary key of the stocks table?
  - Do I want to use stock symbol as a primary key?
    Or do I want to use Database generated primary
    key field?

### Object model
- Does the object model has to match table?

## Designing of REST APIs

- Get all stocks
  - get http://localhost:5000/stocks
  
- Buy and sell (in random order)
  - Do we allow this operation only on existing stock?
 
  - Option #1
    - GET http://localhost:5000/stocks/amzn
    - PUT http://localhost:5000/stocks/amzn with

      ```
      {complete json of stock with "volume" attribute reflects after buy/sell value}
      ```
   - Option #2
    - GET/PUT/POST http://localhost:5000/stocks/amzn?action=buy&volume=100
      - For buy/sell, you can use "GET", "PUT", and "POST"
      - Which one would you like to use?
        - Think about [Idempotency](https://blog.dreamfactory.com/what-is-idempotency/#:~:text=Idempotency%20is%20a%20property%20of%20certain%20operations%20or%20API%20requests,it%20was%20executed%20only%20once.)
      - What happens if the response of "buy/sell" request gets lost?
        Should client send the request again? What would be the consequence?

   - Option #3
     - GET/PUT/POST http://localhost:5000/buy/appl/300 for buying
     - GET/PUT/POST http://localhost:5000/sell/appl/200 for buying
  
  
- A user can see total profit/loss a single point in time
  - Option #1: Do you need to create an API for this? 
    - Example: localhost:5000/stocks/totalProfit
    - Example: localhost:5000/stocks/appl/profit
  - Option #2: Can profit/loss be computed automatically 
    when all stocks are displayed?
    - If you take this approach, where do you do
      this computation, client or server?

## UI

- You are welcome to use your own HTML/CSS but
  feel free to use Bootstrap, which is "simpler
  to use" to create a [Grid](https://www.w3schools.com/bootstrap/bootstrap_grid_system.asp)
- Creating graphical chart 
  is nice to have but
  not critical so consider adding chart only 
  after all the other functionality is finished
  - See [How to create chart using Bootstrap](https://www.geeksforgeeks.org/how-to-create-chart-using-bootstrap/)

## GitHub CoPilot

- Create GitHub account (if you don't have one)
- Go to your Github account page
- Choose "Setting->Try Copilot" and follow instructions
  - You can try 30-day free trial
  - You still have to provide credit card or paypal info.
- On the VSC, install "GitHub Copilot" plug-in
  - Restart VSC
- Write comment and then press CTRL+Return (for both
  Windows and Mac) to generate the example code
