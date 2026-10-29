import java.util.*;

public class LibraryManagement {

    static HashMap<Integer, String> books = new HashMap<>();
    static HashSet<Integer> borrowed = new HashSet<>();
    static Scanner sc = new Scanner(System.in);

    public static void main(String[] args) {

        books.put(101, "Java");
        books.put(102, "Python");
        books.put(103, "Data Structures");

        while (true) {
            System.out.println("\n1. Display Books");
            System.out.println("2. Search Book");
            System.out.println("3. Borrow Book");
            System.out.println("4. Return Book");
            System.out.println("5. Exit");
            System.out.print("Enter choice: ");

            try {
                int choice = sc.nextInt();

                switch (choice) {
                    case 1:
                        System.out.println(books);
                        break;

                    case 2:
                        System.out.print("Enter Book ID: ");
                        int id = sc.nextInt();

                        if (!books.containsKey(id))
                            throw new IllegalArgumentException(
                                "Invalid Book ID!");

                        System.out.println("Book: " + books.get(id));
                        break;

                    case 3:
                        System.out.print("Enter Book ID: ");
                        id = sc.nextInt();

                        if (!books.containsKey(id))
                            throw new IllegalArgumentException(
                                "Invalid Book ID!");

                        if (!borrowed.add(id))
                            throw new IllegalStateException(
                                "Book already borrowed!");

                        System.out.println("Book borrowed successfully!");
                        break;

                    case 4:
                        System.out.print("Enter Book ID: ");
                        id = sc.nextInt();

                        if (!borrowed.remove(id))
                            throw new IllegalStateException(
                                "Book was not borrowed!");

                        System.out.println("Book returned successfully!");
                        break;

                    case 5:
                        System.out.println("Thank you!");
                        sc.close();
                        return;

                    default:
                        System.out.println("Invalid choice!");
                }

            } catch (IllegalArgumentException |
                     IllegalStateException e) {
                System.out.println("Error: " + e.getMessage());

            } catch (InputMismatchException e) {
                System.out.println("Enter a valid number!");
                sc.nextLine();
            }
        }
    }
}
