import java.util.*;

public class PhoneBook {

    public static void main(String[] args) {
        Map<String, Set<String>> phoneBook = new HashMap<>();

        addPhoneNumber(phoneBook, "Alice", "1234567");
        addPhoneNumber(phoneBook, "Bob", "2345678");
        addPhoneNumber(phoneBook, "Charlie", "3456789");
        addPhoneNumber(phoneBook, "Alice", "1111111");
        addPhoneNumber(phoneBook, "Bob", "2222222");
        addPhoneNumber(phoneBook, "Alice", "1234567434");

        List<Map.Entry<String, Set<String>>> list = new ArrayList<>(phoneBook.entrySet());
        Collections.sort(list, new Comparator<Map.Entry<String, Set<String>>>() {
            public int compare(Map.Entry<String, Set<String>> o1, Map.Entry<String, Set<String>> o2) {
                return o2.getValue().size() - o1.getValue().size();
            }
        });

        for (Map.Entry<String, Set<String>> entry : list) {
            System.out.println("Name: " + entry.getKey() + " - Phone Numbers: " + entry.getValue());
        }
    }

    private static void addPhoneNumber(Map<String, Set<String>> phoneBook, String name, String phoneNumber) {
        if (phoneBook.containsKey(name)) {
            phoneBook.get(name).add(phoneNumber);
        } else {
            Set<String> phoneNumbers = new HashSet<>();
            phoneNumbers.add(phoneNumber);
            phoneBook.put(name, phoneNumbers);
        }
    }
}
