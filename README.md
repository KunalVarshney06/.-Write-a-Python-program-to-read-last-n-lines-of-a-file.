# .-Write-a-Python-program-to-read-last-n-lines-of-a-file.
def read_last_n_lines(file_path, n):
    try:
        with open(file_path, 'r') as file:
            lines = file.readlines()
            last_n_lines = lines[-n:]
            for line in last_n_lines:
                print(line.strip())
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
num_lines = 5  # Number of lines to read from the end
read_last_n_lines(file_path, num_lines)
