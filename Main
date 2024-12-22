import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;

public class Main {

    private static boolean isLucky(String t) {
        if (t.length() != 6) return false;
        int a = Character.getNumericValue(t.charAt(0)) + Character.getNumericValue(t.charAt(1)) + Character.getNumericValue(t.charAt(2));
        int b = Character.getNumericValue(t.charAt(3)) + Character.getNumericValue(t.charAt(4)) + Character.getNumericValue(t.charAt(5));
        if (a != b) return false;
        Set<Character> s = new HashSet<>();
        for (char c : t.toCharArray()) if (!s.add(c)) return false;
        return true;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Iveskite bilieto numeri: ");
        String t = sc.nextLine().trim();

        if (t.matches("\\d{6}") && isLucky(t)) {
            System.out.println("Bilietas " + t + " laimingas");
        } else {
            System.out.println("Bilietas " + t + " nelaimingas");

            int c = 0;
            while (true) {
                c++;
                int r = (int) (Math.random() * 1000000);
                String f = String.format("%06d", r);
                if (isLucky(f)) {
                    System.out.println("Laimingas bilietas: " + f);
                    System.out.println("Bandymu skaicius: " + c);
                    break;
                }
            }
        }
        sc.close();
    }
}
