<h1 align="center"> Secret Auction Program</h1>

I have created  program to run a secret auction. Users are prompted to enter their name and bid amount, which is privately disclosed by clearing the output with newline characters. The program can loop through to add additional bidders. The name and bid amount of all bidders is saved into the bid dictionary. The program then selects the name and amount of the highest bidder! 

This program can be used for small group auctions, charity fundraisers, or classroom games where participants place secret bids.

```
import art
print(art.logo)

def find_highest_bidder(bidding_dictionary):
    winner = ""
    highest_bid = 0
    for bidder in bidding_dictionary:
        bid_amount = bidding_dictionary[bidder]
        if bid_amount > highest_bid:
            highest_bid = bid_amount
            winner = bidder

    print(f"The winner is {winner} with a bid of {highest_bid}.")

bid_data = {}
continue_bidding = True
while continue_bidding:
    name = input("What is your name?: ")
    price = float(input("What is your bid: $"))
    bid_data[name] = price
    new_bids = input("Are there others bidders? Type 'yes' or 'no'.\n").lower()
    if new_bids == 'no':
        continue_bidding = False
        find_highest_bidder(bid_data)
    elif new_bids == 'yes':
        print("\n" * 20)
```

Here is a test case displaying the user experience from my editor:
```
                         ___________
                         \         /
                          )_______(
                          |"""""""|_.-._,.---------.,_.-._
                          |       | | |               | | ''-.
                          |       |_| |_             _| |_..-'
                          |_______| '-' `'---------'` '-'
                          )"""""""(
                         /_________\\
                       .-------------.
                      /_______________\\

What is your name?: Rachel
What is your bid: $350.00
Are there others bidders? Type 'yes' or 'no'.
yes





















What is your name?: Jacob
What is your bid: $400.00
Are there others bidders? Type 'yes' or 'no'.
yes





















What is your name?: Nate
What is your bid: $210.00
Are there others bidders? Type 'yes' or 'no'.
no
The winner is Jacob with a bid of 400.0.
```
