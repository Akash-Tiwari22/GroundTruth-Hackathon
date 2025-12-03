ShopBuddy AI – Hyper-Personalized Customer Support Agent

Tagline: An AI-powered chat-first support agent that detects your live location, fetches store & inventory data, and delivers personalized suggestions while masking sensitive information.

1. The Problem (Real World Scenario)

Context: Retail customers expect instant answers. Standard chatbots give generic responses and fail to consider location, purchase history, or context.

The Pain Point: Customers asking questions like “Is the store open?” or “Do you have Hot Cocoa?” often get delayed or irrelevant answers. Businesses lose engagement and may miss opportunities to drive sales.

My Solution: I built ShopBuddy AI, a 2-screen chat-first MVP. The user’s live location is detected automatically. When a user interacts with the bot, it fetches nearby store info, inventory, and personalized recommendations. All sensitive user data is masked before sending it to AI.

2. Expected End Result

For the User:

Input: Open the app → ShopBuddy detects live location → Start chatting.

Action: Ask questions like “I’m cold” or “Do you have cappuccino?”

Output: Receive a conversational experience with:

Nearby store info card (open/close status, distance)

Inventory card (product availability, quantity)

Personalized suggestions (e.g., “You seem cold — Hot Cocoa is available 50m away. Want 10% off?”)

Inline action buttons: “Order for Pickup”, “Apply 10% Coupon”

3. Technical Approach

Goal: Build a production-ready MVP with hyper-personalization, live location awareness, and privacy-first AI, all in a chat-first interface.

System Architecture:

Screen 1 – Welcome / Store Detection:

Detect nearby store using live location.

Show store card with open/close status, distance, and primary CTA (“Start Chatting”).

Display privacy note: “Your data stays protected — sensitive info is masked before AI processing.”

Screen 2 – Smart Chat Support:

Chat interface with user + bot bubbles.

Inline AI-generated Cards:

Store Info Card: name, status, distance, “Show Directions” button.

Inventory Card: product thumbnail, status, quantity, “Apply 10% Coupon” button.

Personalized Suggestion Bubble: context-aware recommendations.

Order CTAs: “Order for Pickup” / “Suggest alternatives”.

Privacy Integration:

Phone numbers masked: +91-XXXXXXXXXX

Emails masked: a***@gmail.com

All PII masked before AI processing

RAG (Retrieval-Augmented Generation):

Fetches: store hours, inventory, user purchase history (mocked)

Responses are inline, context-aware, and location-sensitive

Behavior / UX:

Auto-scroll on new messages

Smooth reveal animations

Inline CTAs, no extra screens

4. Tech Stack

Frontend: React.js / React Native

Styling & Animations: Tailwind CSS / Framer Motion

Backend: Node.js + Express.js

RAG / Knowledge Retrieval: Vector store (FAISS / Pinecone)

AI Model: GPT / Google Gemini (mocked for demo)

Privacy Masking: Custom middleware

Location Detection: Browser Geolocation API / React Native Geolocation

5. Challenges & Learnings

Challenge 1 – Live Location Context

Issue: Personalized suggestions must reflect nearby stores accurately.

Solution: Implemented geolocation API and distance calculations to deliver precise suggestions in chat.

Challenge 2 – Privacy Compliance

Issue: User PII could be exposed to AI.

Solution: Middleware masks phone numbers, emails, and order IDs before sending to AI.

Challenge 3 – Chat-First UX

Issue: Multiple screens made demo flow complex.

Solution: All interactions, cards, and actions are embedded inline in a single chat screen.

6. Visual Proof

Welcome / Store Detection Screen: Shows nearby store based on live location, open/close status, and privacy note.

Smart Chat Support Screen:

Store Info Cards

Inventory Cards

Personalized Suggestion Bubbles

Inline action buttons: “Order for Pickup”, “Apply 10% Coupon”

7. How to Run
1. Clone Repository
git clone https://github.com/username/shopbuddy-ai.git
cd shopbuddy-ai

2. Install Dependencies
npm install   # Frontend
npm install   # Backend

3. Add API Key (for AI Model if using GPT/Gemini)
export AI_API_KEY="your_key_here"

4. Start Backend
node server.js

5. Start Frontend
npm start

6. Test Demo Flow

Launch app → Welcome screen → Live store detection → Start Chatting

Try messages:

“I’m cold” → Hot Cocoa suggestion

“Do you have cappuccino?” → Inventory card

“Is the store open?” → Store info card
<img width="1390" height="737" alt="Screenshot 2025-12-03 at 11 50 29 AM" src="https://github.com/user-attachments/assets/d40873e2-1551-4dee-8ab5-d775352e67e3" />

<img width="1433" height="729" alt="Screenshot 2025-12-03 at 11 51 51 AM" src="https://github.com/user-attachments/assets/0a3bbb42-6321-4570-a75b-308d38de8bb8" />

<img width="1455" height="744" alt="Screenshot 2025-12-03 at 11 52 26 AM" src="https://github.com/user-attachments/assets/06dc6c45-251b-4296-b2b0-450ffff5652c" />








