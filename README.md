
class ShoppingList:
    de __init__(self):
        self.ite = []

    def add_item(self, items):
        if item in self.items:
            print(f"'{item}' is already in the shopping list.")
        else:
            self.items.append(item)
            print(f"Added '{item}' to the shopping list.")

    def remove_item(self, item):
        if item in self.items:
            self.items.remove(item)
            print(f"Removed '{item}' from the shopping list.")
        else:
            print(f"'{item}' not found in the shopping list.")

    def show_items(self):
        if not self.items:
            print("The shopping list is empty.")
        else:
            print("Shopping list items:")
            for idx, item in enumerate(self.items, start=1):
                print(f"{idx}. {item}")

    def search_item(self, keyword):
        found_items = [item for item in self.items if keyword.lower() in item.lower()]
        if found_items:
            print("Search results:")
            for item in found_items:
                print(f"- {item}")
        else:
            print(f"No items found containing '{keyword}'.")

def main():
    shopping_list = ShoppingList()
    while True:
        print("\n--- Shopping List Manager ---")
        print("1. Add item")
        print("2. Remove item")
        print("3. Show all items")
        print("4. Search for an item")
        print("5. Exit")
        choice = input("Enter your choice (1-5): ")

        if choice == '1':
            item = input("Enter the item to add: ")
            shopping_list.add_item(item)
        elif choice == '2':
            item = input("Enter the item to remove: ")
            shopping_list.remove_item(item)
        elif choice == '3':
            shopping_list.show_items()
        elif choice == '4':
            keyword = input("Enter keyword to search: ")
            shopping_list.search_item(keyword)
        elif choice == '5':
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please select a number from 1 to 5.")

if __name__ == "__main__":
    main()
