# Seinfield-TV-Show-Script-Generator

## Data
9 Seasons of Seinfield TV Shows
Stored in csv file

## Preprocessing Data
1. Create a look up table map word to number
2. Replace punctuation and specific characters with number

## Build & Train Model
1. Pass word to an Embedding layer with 400 dimension to get the vector representation of that word
2. Pass the word vector to Seq-to-Seq model with 2 LSTM layer
3. Given a Sequence of 10 words, aim to predict the 11th word
4. Train epochs: 10
5. Leaning rate: 0.001

## Testing Model or Generate Sequence
1. Initialize a sentence with 10 words
2. Predict the next 11th word
3. Choose top 5 words that has highest probability to become the 11th word
4. Randomly choose 1 of those 5 words and assign it to the 11th word
5. Fit the model with new sequence of 2nd word --> 11th word
6. Keep going like that to generate the new TV Scipt
7. Stop if the model ouput the speical character "||END||"


