

- [Requirement](#requirement)
- [Development methodology](#development-methodology)
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
        that gets the real-time stock price value
    - UI    
      - Use simplest UI possible
      - Draw wireframes for UI
    - Start something simple
      - For example, make end-to-end operation work
        for displaying all stocks first
      - Then add feature incrementally
  - Work in two-hour SPRINT cycles

## Designing of REST APIs

- Get all stocks
  - get http://localhost:5000/stocks
- Buy and sell 
  - Option #1
    - get/post http://localhost:5000/stocks/amzn?action=buy&volume=100
      - For buy/sell, you can use either"get" and "post"
      - Which one would you like to use?
      - See [how to get request parameter values](https://stackabuse.com/get-request-query-parameters-with-flask/) 
        for example code

  - Option #2
    - post http://localhost:5000/transactions/ with
      
      ```
      {"action": "buy", stock: "AMAZN", "volume": 100}
      ```
  - Option #3
    - put http://localhost:5000/stocks/amzn with

      ```
      {complete json of stock}
      ```
    
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
- [Creating graphical chart](https://mdbootstrap.com/docs/standard/data/charts/) 
  is nice to have but
  not critical so consider adding chart only 
  when all the other functionality is finished
- Alternative to the above, using [FOSS](https://www.geeksforgeeks.org/how-to-create-chart-using-bootstrap/)

## GitHub CoPilot

- Create GitHub account (if you don't have one)
- Go to your Github account page
- Choose "Setting->Try Copilot" and follow instructions
  - You can try 30-day free trial
  - You still have to provide credit card or paypal
- On the VSC, install "GitHub Copilot" plug-in
  - Restart VSC
- Write comment and then press CTRL+Return (for both
  Windows and Mac) to generate the code
