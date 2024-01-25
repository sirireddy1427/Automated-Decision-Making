# Automated-Decision-Making
Developed a Automated Decision making system that picks a movie or series based on user prefered genre 
import random

# Define the genres and corresponding movies and series
genres = {
    'Action': {'Movies': ['Saalar', 'Leo', 'Animal', 'Revenge', 'War'],
               'Series': ['Money Heist', 'Lucifer', 'Khakee: The Bihar Chapter', 'Fauda', 'Sacred Games']},
    'Comedy': {'Movies': ['Ante Sundaraniki', 'Don', 'Mad', 'Ms Shetty Mr Polishetty', 'Jathi Ratnalu'],
               'Series': ['Friends', 'Mismatched', 'Young Sheldon', 'The Office', 'Welcome to Waikiki']},
    'Crime': {'Movies': ['Saakini Daakini', 'Neevevaro', 'Red', 'Thimmarusu', 'Pink'],
              'Series': ['Killer Soup', 'Breaking Bad', 'Guns and Gulaabs', 'House of Secrets: The Burari Deaths', 'She']},
    'Drama': {'Movies': ['Gangubai Kathiawadi', 'Awe', 'Shyam Singha Roy', 'Hi Nanna', 'Three of Us'],
              'Series': ['Emily in Paris', 'Maid', 'Celebrity', 'Bombay Begums', 'Rana Naidu']},
    'Documentaries': {'Movies': ['Curry and Cyanide', 'The Elephant Whisperers'],
                      'Series': ['Indian Predator: The Butcher of Delhi', 'Beast of Bangalore',
                                 'Indian Predator: The Diary of a Serial Killer', 'Indian Predator: Murder in a Courtroom',
                                 'The Hunt for Veerapan']},
    'Horror': {'Movies': ['The Pope's Exorcist', 'The Conjuring', 'Ouija', 'Chandramukhi', 'Virupaksha'],
               'Series': ['Locke & Key', 'Wednesday', 'All of Us Are Dead', 'The Haunting of Hill House', 'Black Summer']},
    'Romance': {'Movies': ['Ae Dil Hai Mushkil', 'Meenakshi Sundareshwar', 'Jaane Tu Ya Jaane Na', 'Dil Se', 'OK Kanmani'],
                'Series': ['Tooth Pari', 'Mismatched', 'A Suitable Boy', 'Gossip Girl']},
    'Sci-Fi': {'Movies': ['The In Between', 'Oxygen', 'The Adam Project', 'Spiderhead'],
               'Series': ['Stranger Things', 'V Wars', 'Travelers', 'The Mist', 'Salvation']},
    'Thriller': {'Movies': ['Roja', 'Haseen Dilruba', 'Buttabomma', 'O Pitta Katha', 'Karthik Calling Karthik'],
                 'Series': ['The Recruit', 'Alice in Borderland', 'Lupin', 'My Name', 'Kingdom']}
}

# Get user input for genre
print("Choose a genre:")
for index, genre in enumerate(genres.keys(), start=1):
    print(f"{index}. {genre}")

selected_genre_index = int(input("Enter the number corresponding to your desired genre: "))
selected_genre = list(genres.keys())[selected_genre_index - 1]

# Get user input for movie or series
media_type = input("Do you want to watch a movie or series? Enter 'movie' or 'series': ")

# Randomly select a movie or series from the chosen genre
if media_type.lower() == 'movie':
    selected_content = random.choice(genres[selected_genre]['Movies'])
elif media_type.lower() == 'series':
    selected_content = random.choice(genres[selected_genre]['Series'])
else:
    print("Invalid input. Please enter 'movie' or 'series'.")

# Display the recommendation
print(f"Recommended {media_type} for you: {selected_content}")
