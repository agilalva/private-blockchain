# Private Blockchain Application

You are starting your journey as a Blockchain Developer, this project allows you to demonstrate
that you are familiarized with the fundamentals concepts of a Blockchain platform.
Concepts like: - Block - Blockchain - Wallet - Blockchain Identity - Proof of Existance

Are some of the most important components in the Blockchain Framework that you will need to describe and also
why not? Implement too.

In this project you will have a boilerplate code with a REST Api already setup to expose some of the functionalities
you will implement in your private blockchain.

## What problem will you solve implementing this private Blockchain application?

Your employer is trying to make a test of concept on how a Blockchain application can be implemented in his company.
He is an astronomy fans and he spend most of his free time on searching stars in the sky, that's why he would like
to create a test application that will allows him to register stars, and also some others of his friends can register stars
too but making sure the application know who owned each star.

### What is the process describe by the employer to be implemented in the application?

1. The application will create a Genesis Block when we run the application.
2. The user will request the application to send a message to be signed using a Wallet and in this way verify the ownership over the wallet address. The message format will be: `<WALLET_ADRESS>:${new Date().getTime().toString().slice(0,-3)}:starRegistry`;
3. Once the user have the message the user can use a Wallet to sign the message.
4. The user will try to submit the Star object for that it will submit: `wallet address`, `message`, `signature` and the `star` object with the star information.
   The Start information will be formed in this format:
    ```json
        "star": {
            "dec": "68° 52' 56.9",
            "ra": "16h 29m 1.0s",
            "story": "Testing the story 4"
    	}
    ```
5. The application will verify if the time elapsed from the request ownership (the time is contained in the message) and the time when you submit the star is less than 5 minutes.
6. If everything is okay the star information will be stored in the block and added to the `chain`
7. The application will allow us to retrieve the Star objects belong to an owner (wallet address).

## Screenshots

1. Request the Genesis block:
<img width="1392" alt="genesis block" src="https://user-images.githubusercontent.com/7228491/122655617-8b044f80-d14b-11eb-8d72-fd64f7c1c917.png">
2. Request of ownership sending the wallet address:
<img width="1392" alt="request ownership" src="https://user-images.githubusercontent.com/7228491/122655687-31505500-d14c-11eb-9cb9-d634c027ba2d.png">
3. Sign the message with the wallet (Electrum):
<img width="985" alt="Sign message" src="https://user-images.githubusercontent.com/7228491/122655691-3ca38080-d14c-11eb-8b57-80c3e7a56389.png">
4. Submit the star:
<img width="1392" alt="Submit star" src="https://user-images.githubusercontent.com/7228491/122655694-41683480-d14c-11eb-8952-39dc5e4d7141.png">
5. Retrieve stars owned by address:
<img width="1392" alt="Get stars by wallet address" src="https://user-images.githubusercontent.com/7228491/122655696-46c57f00-d14c-11eb-8640-62e611120759.png">
