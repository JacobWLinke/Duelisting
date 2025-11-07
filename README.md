# Duelisting: a Secure Yu-Gi-Oh! Deck Architechture app

Instead of using insecure browser tabs and fragmented lists to hone the perfect Yu-Gi-Oh! deck, Duelisting provides a secure, real-time web application that allows players to structure their decks with privacy and catalogue their wins with accuracy. Duelisting isn't just a simple list of cards, it is a fully authenticated, private vault where players can construct, analyze, and securely store their competitive deck builds.
Duelisting ensures that a player's proprietary strategies remain confidential and protected from unauthorized access until they are ready to be unveiled in play. It provides a clean, interface for searching the card library, building decks up to the 60-card limit, and maintaining strict version history, all while adhering to the principle of least privilege in its user and data management. Duelisting is the secure foundation for competitive duelists to architect their wins.

# Installation

Duelisting is containerized for maximum security and ease of deployment.

Prerequisites

You must have Docker and Docker Compose installed on your system.

Build and Setup

1. Clone the repository

git clone [https://github.com/your-username/Duelisting.git](https://github.com/your-username/Duelisting.git)
cd Duellisting

2. Build the application and database images

docker compose build

3. Initialize the database and apply schema migrations

docker compose run --rm web python manage.py migrate


# Getting Started
To run the application locally, use the following command:

Start the web server and database in detached mode
docker compose up -d


The application will be accessible in your web browser at http://localhost:8000/.

To stop the application:

docker compose down


# License 
The MIT License (MIT)
Copyright (c) [Jacob Linke] [2025]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

# Note on LLM Usage
Portions of the code and documentation within this repository were generated or refined using a Large Language Model (LLM) for efficiency. However, the author, JacobWLinke, retains full creative responsibility for the application's design, architectural decisions, security implementation, and code integrity. All code has been reviewed, tested, and maintained by the primary author.
