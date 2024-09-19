def spoiler_blocker(text, keywords):
    for keyword in keywords:
        text = text.replace(keyword, '[SPOILER]')
    return text

def main():
    print("Welcome to the Spoiler Blocker!")
    
    # Get input text from the user
    text = input("Enter the text you want to process:\n")
    
    # Get keywords to block
    keywords_input = input("Enter keywords to block, separated by commas:\n")
    keywords = [keyword.strip() for keyword in keywords_input.split(',')]
    
    # Process the text
    processed_text = spoiler_blocker(text, keywords)
    
    print("\nProcessed Text:")
    print(processed_text)

if __name__ == "__main__":
    main()
