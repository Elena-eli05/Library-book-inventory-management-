def add_book(library, title, quantity):
    if title in library:
        library[title] += quantity 
    else:
        library[title] = quantity  
    print(f'Book "{title}" added successfully')

def remove_book(library, title):
    if title in library:
        del library[title]
        print(f'Book "{title}" removed from inventory.')
    else:
        print(f'Book "{title}" not found')

def update_quantity(library, title, quantity):
    if title in library:
        library[title] = quantity
        print(f'Quantity of "{title}" updated to {quantity}.')
    else:
        print(f'Book "{title}" not found')

def search_book(library, title):
    if title in library:
        print(f'Book Found - Title: {title}, Quantity: {library[title]}')
    else:
        print(f'Book "{title}" not found')

def display_books(library):
    if library:
        print("\nLibrary Inventory:")
        for title, quantity in library.items():
            print(f'Title: {title}, Quantity: {quantity}')
    else:
        print("Library is empty")


library = {}

add_book(library, "Harry Potter", 6)
add_book(library, "1984", 3)
add_book(library, "Gitanjali", 10)
display_books(library)
search_book(library, "1984")
search_book(library, "Invisible Man")
update_quantity(library, "1984", 7)
display_books(library)
remove_book(library, "1984")
display_books(library)
