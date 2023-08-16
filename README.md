# Polkadot Staking Troubleshooting

This README.md explains the possible error and success messages that can be thrown by the provided HTML code for Polkadot staking troubleshooting.

Please note that everything is setup in one HTML file so the code can run in various applications/internal tools by simply pasting the code into an HTML addition.

## Possible Error and Success Messages

All error/success messages are displayed within the balance table

### 1. Account Balance and Staking Info

- **Error (Address Empty):** If the user clicks the "Run" button without entering a Polkadot address, the code will not proceed and no messages will be displayed.

- **Error (Account Not Staking):** If the account has a balance but is not staking, an error message will be displayed: "Account not staking."

- **Error (Account Has No Balance):** If the account has no balance, an error message will be displayed: "Account has no balance."

### 2. Staking Threshold and Suggestions

- **Success:** Success message "You should be earning rewards" will display if no issue/error comes up when running through the different requests via Polkadot-JS API. If there is even one of the following issues/errors, error messages will be thrown for them, and no success message will show. 

- **Issue (Low Staking Balance):** If the staked balance is below the minimum threshold for rewards, the following message will be displayed:
  - "It is suggested to have the staking threshold ([minimum threshold]) + 20 to earn rewards."
  - "Try staking at least [additional amount needed] more DOT to earn rewards."

### 3. Nominations and Validator Info

- **Success (16 Nominations):** If the account has nominated 16 validators, a success message will be displayed: "You should be earning rewards."

- **Issue (Less than 16 Nominations):** If the account has nominated less than 16 validators, an issue message will be displayed: "Nominate 16 validators for the best chance at earning consistent rewards. You currently have [number of validators nominated] validator(s) nominated."

- **Issue (High Commission Validators):** If all or some nominated validators have a high commission (100%), error messages will be displayed:
  - "All ([number of validators]) validator(s) nominated have 100% commission."
  - "Some ([number of validators]) validator(s) nominated have 100% commission."

- **Issue (Commission Issue):** If there is an issue with validator commissions, a general issue message will be displayed: "You may or may not earn rewards consistently due to current validators nominated (commission issue)."

### 4. General Errors

- **Error (Fetching Data):** If there is an issue with fetching data from the Polkadot network, the code will display an error message: "error, retry."

## Instructions

1. Navigate to https://polkadot-staking-test.web.app/, or run HTML locally.
2. Enter a valid Polkadot address in the input field.
3. Click the "Run" button to fetch and display staking and nomination information.

Please note that the success and error messages are provided as placeholders. You can modify and customize these messages based on your application's requirements and the specific scenarios you want to handle.