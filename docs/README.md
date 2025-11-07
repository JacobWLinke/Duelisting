## User Stories

As a new Duelisting user, I want to create a secure user account, so I can access the deck building tools and save my work privately.
  #### Acceptance Criteria: 
  1. System validates that the password meets minimum complexity requirements (length, characters). 2. The user receives confirmation of successful registration. 3. The system securely hashes and salts the password before storing it.
  
As a Duelisting user, I want to search for specific cards in the card library, so I can quickly find the card that I need for my specific strategy.
  #### Acceptance Criteria: 
  1. Search results update in real-time as the user types. 2. Card results display the card name and type. 3. The search function handles special characters and common abbreviations.
  
As a Duelisting user, I want to add cards to a new or existing deck, so I can construct a complete deck that adheres to the rules of Yu-Gi-Oh!
  #### Acceptance Criteria: 
  1. The deck view updates instantly when a card is added or removed. 2. The system prevents a user from adding more than three copies of any non-limited card. 3. The system displays a counter for current deck size and the number of specific card types (Monster, Spell, Trap).
  
As a Duelisting user, I want to access only the decks that I created from my dashboard, so I can be certain my proprietary strategies are protected. 
  #### Acceptance Criteria: 
  1. The dashboard query filters decks by the current authenticated user ID. 2. Attempts to load another user's deck via a manipulated URL fail and return a 403 Forbidden error.
  
As a Duelisting administrator, I want to delete inappropriate user content, so I can maintain a compliant environment. 
#### Acceptance Criteria: 
  1. Only users with the Admin role can see the delete button for any deck. 2. Deletion requires an explicit confirmation step.

## Mis-User Stories

As an unauthenticated attacker, I want to bypass the login page, so I can view other users' private decks.
  #### Mitigation Criteria:
  1. Authentication: All routes for deck management and viewing are protected by session checks. 

As an authenticated attacker, I want to view or edit another users' private decks by changing the ID in the URL, so I can disrupt their preparation for competition and steal their strategies.
  #### Mitigation Criteria:
  1. Authorization: Every database query retrieving a deck must explicitly check that the deck.owner_id matches the current authenticated user. 

As an attacker using Rate Limit Bypass, I want to attempt thousands of password guesses against a user's account, so I can perform a brute-force attack and gain unauthorized access.
  #### Mitigation Criteria: 
  1. Rate Limiting: The login endpoint is rate-limited to a maximum of 5 failed attempts per IP address per minute. 2. Account Lockout: An account is locked out for 10 minutes after 10 failed login attempts.

## Diagrams

  #### Mockup
  View 1: Login Screen
  
  ![Mockup_View1](https://github.com/user-attachments/assets/7afd7182-01e3-4d12-b3b5-4a8b2c3b9219)

  View 2: User Dashboard
  
  ![Mockup_View2](https://github.com/user-attachments/assets/b62c9001-08c0-46f7-964c-35a7d8a810a2)

  View 3: Deck Builder
  
  ![Mockup_View3](https://github.com/user-attachments/assets/15472dfc-0a8e-40d1-9d6d-f30ff3c1a54a)

  #### Architechture

  C1: System Context Diagram
  
  ![Architecture_C1](https://github.com/user-attachments/assets/2d2bfa0b-e33c-419f-ba1a-9f7b53b4b7e7)

  C2: Container Diagram
  
  ![Architecture_C2](https://github.com/user-attachments/assets/f7934b7d-7455-4f9f-b057-d865ef5fb4c1)

  C3: Component Diagram
  
  ![Architecture_C3](https://github.com/user-attachments/assets/fc6de011-decb-4e06-8604-dee8a31a0bd3)


  


  


