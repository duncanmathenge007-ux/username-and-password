import java.util.Scanner;

public class SimpleLogin {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        String correctUser = "dun";
        String correctPass = "12345";

        int attempts = 0; 

        
        while (attempts < 3) {
            System.out.print("Username: ");
            String user = sc.nextLine();

            System.out.print("Password: ");
            String pass = sc.nextLine();

        
            for (int i = 0; i < pass.length(); i++) {
                System.out.print("*");
            }
            System.out.println(); 

        
            if (user.equals(correctUser) && pass.equals(correctPass)) {
                System.out.println("Login successful!");
                return; 
            } else {
                System.out.println("Wrong username or password.");
                attempts++; 
            }
        }

        System.out.println("Access denied. Too many attempts.");
        sc.close();
    }
}
