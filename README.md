<img width="463" alt="Screenshot 2024-08-28 at 17 47 53" src="https://github.com/user-attachments/assets/abe83c96-0e71-4a80-83de-dfc1926ada2a"># Web Home Task

1. Create a new private repo and invite: @mario-deblock.
2. Start or upload your project.
3. We take into account:
  - Use Typescript + ReactJS
  - SOLID principles, clean architecture and good separation of concerns BUT without over-engineering.
  - Pixel perfect approach, product is the most important topic at Deblock. 

## Requirements

### Design
<img width="463" alt="Screenshot 2024-08-28 at 17 47 53" src="https://github.com/user-attachments/assets/d5fa4a32-3475-40e9-8797-7db5945f2356">

FIGMA file to follow soon.

### Features
We want a web app where the user can:
1/ Allow a user to connect their metamask wallet via any web3 provider library. (Feel free to draft a simple "Connect button" on the navBar, or a login page with it, no design provided, surprise us :) 
2/ Once a wallet is connected, we want users to be able to get exchange rates between ETH and different pairs (for example USDT, and BTC), with the provided component. 

In this screen (ignore the keyboard, only needed in native mobile apps):
- As a user I can exchange ETH for other currencies, but I can select which one on the Your Receive currencies with a selector. Ignore the design in terms of "You Pay". "You Pay" is fixed to just ETH.
From there, the user will get 2 different quotes:
- As a user I can select an amount on the "You Pay" and will get the equivalent exchange rate in the "You Receive". The "You Receive" selector should contain "USDT" and "BTC".
- As a user I can see the estimated exchange rate into EUR for the amount "You Pay" in the bottom right

In the "You Pay" use ETH
In the "You Receive" use USDT, BTC

You will need to consume this API data points for the exchange rates:
1. Exchange rate (Crypto to eur/gbp/usd)

#### Obtaining Exchange rate

For the exchange rate, you can consume any free API, but here you have a working example you can use:

**Request**
```
https://api.coingecko.com/api/v3/simple/price?ids=ethereum&vs_currencies=usd
```

**Response**
```
{
  "ethereum": {
    "eur": 1644.1
  }
}
```

`vs_currencies` accepts `eur`, 
`ids` accepts "tether" (USDT) and "bitcoin" (BTC) and "ethereum" (ETH)

## What we look for
- Be pixel perfect
- Animate the modal
- Clean code
- Be fast and work with "meh" specifications like this one (lets be real, sometimes happens).

