# cook

**_Let Them Cook_** is a recipe AI that generates fridge-cleaning recipes based on your fridge - beneficial for both your wallet and the world! 🧑‍🍳

Nearly 40% of food in the U.S. is wasted. For our submission for CalHacks AI Hackathon 2023 (Jun 17–18, 2023), we wanted to tackle this problem. Our project placed in the top 50% of >200 teams!

#### Full Devpost for more info & pictures: https://devpost.com/software/let-them-cook-9yb6za 🍓🍳🐟

**Frontend**
- Generating recipes based on the ingredients available in the user's fridge, with a 3-step process:
  1. Scan the user's fridge through their mobile camera to identify ingredients
  2. Displays the detected ingredients for the user to review and modify
  3. Generate recipes that maximize the use of these ingredients, providing recipe names, images, and descriptions, and the source cooking website.
- Additional features include recent recipes and access to the entire recipe database. Users can also search for recipes based on specific criteria such as 'vegetarian' or 'easy to cook.' 

**Backend**
- LLMs are used in 3 key aspects: scanning the fridge, generating recipes, and creating appetizing images and descriptions
- The fridge scanning process involves sending the user's fridge image to BLIP-2 with a prompt specifying the ingredients.
- Recipe generation relies on comparing the updated ingredient list with a recipe dataset to identify the top 10 recipes that match the most ingredients.
- DALL-E is used to generate images of the dishes, and GPT-4 creates descriptions.
- Pinecone is used for efficient dataset storage.
- Langchain's similarity_search API to compare user input with the recipe database, resulting in tailored recipe suggestions.







