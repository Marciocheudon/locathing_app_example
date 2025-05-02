# Locathing Flutter Demo
A clean and modern example of integrating the Locathing SDK — a lightweight Dart client for powerful address search and geocoding using the Locathing REST API.

![Locathing Banner](https://github.com/Marciocheudon/locathing_app_example/raw/main/assets/locathinglogo.png)


# Overview
This demo project shows how to use the locathing_sdk package in a Flutter app. With it, you can:

# Perform real-time address searches.

![Locathing Banner](https://github.com/Marciocheudon/locathing_app_example/raw/main/assets/mainpage.png)


## Filter results based on geographic proximity.

## Track your API usage and quota in real-time.

# Tech Stack
Flutter 3.7+

locathing_sdk

http for API requests

flutter_dotenv for managing API keys securely

## Installation
1. Clone this repository
bash

git clone https://github.com/Marciocheudon/locathing_app_example.git
cd locathing_flutter_demo
2. Install dependencies
bash

flutter pub get
3. Set up your .env file
Create a .env file in the root of your project and add your Locathing API key:

# env

LOCATHING_API_KEY=your_api_key_here
Make sure to add .env to your .gitignore file to avoid leaking your key.

# Running the app
bash

flutter run
You can search for addresses, and results will appear instantly as you type.

# How it works
The app uses LocathingClient.search() to fetch address suggestions based on user input. Results are updated on each change, and filtered by proximity for relevance.

dart

final (results, _) = await client.search(
  query: 'Av Paulista',
  type: 'address',
  proximity: '-46.6388,-23.5489',
);

## License
This project is licensed under the MIT License.

