# python-assignment-week-4
ANSWER
# File Read & Write + Error Handling Program

def read_and_modify_file():
    filename = input("Enter the name of the file to read: ")

    try:
        with open(filename, 'r') as infile:
            content = infile.read()

        # Modify the content (example: convert to uppercase)
        modified_content = content.upper()

        # Write modified content to a new file
        new_filename = "modified_" + filename
        with open(new_filename, 'w') as outfile:
            outfile.write(modified_content)

        print(f"✅ Successfully wrote modified content to '{new_filename}'.")

    except FileNotFoundError:
        print("❌ Error: The file does not exist.")
    except IOError:
        print("❌ Error: The file cannot be read or written.")
    except Exception as e:
        print(f"❌ An unexpected error occurred: {e}")

# Run the function
read_and_modify_file()

