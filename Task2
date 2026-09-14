stock_prices = {
    "AAPL": 180,
    "TSLA": 250,
    "GOOGL": 140,
    "MSFT": 350,
    "AMZN": 130
}

portfolio = {}
total_value = 0

print("Available stocks:", list(stock_prices.keys()))

n = int(input("How many different stocks you want to buy? "))

for i in range(n):
    stock = input(f"Enter stock {i+1} name: ").upper()
    qty = int(input(f"Enter quantity of {stock}: "))

    if stock in stock_prices:
        portfolio[stock] = qty
        total_value += stock_prices[stock] * qty
    else:
        print(f"{stock} not found in price list!")

print("\n--- Your Portfolio ---")
for stock, qty in portfolio.items():
    value = stock_prices[stock] * qty
    print(f"{stock}: {qty} x ${stock_prices[stock]} = ${value}")

print(f"\nTotal Investment Value: ${total_value}")

# Optional: Save to file
with open("portfolio.txt", "w") as f:
    f.write(f"Total Investment: ${total_value}\n")
    for s, q in portfolio.items():
        f.write(f"{s} - {q} qty\n")
print("Saved to portfolio.txt")