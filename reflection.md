# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
        When the player makes a guess, the game incorrectly tells the player to guess lower or higher. The game accepts numbers out of the range 1 to 100. After a game is won and the player clicks new game, the game no longer accepts guesses because the guess history is not cleared. The box that accepts answers tells the player to click enter to submit their guess, but clicking enter does not do anything. The initial game gives the player only 7 guesses but they should get 8 guesses. 


**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| guess of 50 | "too low" | "go lower" | none |
| guess of -10 | "out of range" | "go lower" | none |
| player clicks new game and submits a guess| "too low" | "none" | "none"|

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

I used claude code and asked it to explain check_guess(). It caught the error that the game gave the player the wrong feedback. It suggested switching the "Go HIGHER" and "Go LOWER" messages. It also said that the inputs are compared lexicographically which may cause unexpected behavior, but I decided not to make any changes to that right now and only focused on integer input. 
---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

AI helped me implement enough tests to verify that the high/low bug was fixed. I decided that the bug was truly fixed after running these tests and running the game. 
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

A rerun occurs each time the user interacts with the interface. The session state saves information so that progress isn't lost between each rerun.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

One habit is that when asking AI how to do something, it's important to specify that the AI doesn't change the code yet. 
I like to ask for an explanation so that I understand what the AI is going to do. 

Next time I work with AI, I would ask it to tackle one thing at a time. 
I shouldn't tell it to solve two problems simultaneously unless they are closely related. 

This project helped me understand that the AI needs guidance and details so that it behaves the way I want it to. 
