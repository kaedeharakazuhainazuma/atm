package com.mycompany.automatedtellermachine;
import java.util.Scanner;

public class Automatedtellermachine {
    
    static Scanner input = new Scanner(System.in);
    static double savingAmt = 1000;
    static double checkingAmt = 5000;
    
    public static void main(String[] args) {
        // Initialize  variables
        String pin="", correctPin="6767";
        int attempts=0;
        boolean isAuthorized = false;

        
        // 1. Login Loop
        System.out.println("==== Welcome to BSU-CICT Bank ====");
        while (attempts<3 && !isAuthorized){
            System.out.print("Please enter your 4-digit PIN: ");
            pin=input.nextLine();
            
            if (pin.equals(correctPin)){ 
                System.out.println("Please Wait...\n");
                isAuthorized = true;
            }
            else {
                attempts++;
                int triesLeft = 3-attempts;
                
                if (triesLeft > 0){
                System.out.println("Incorrect PIN. You have " + triesLeft + " attempt(s) left.\n");
                }
            }
        }    
        
        // 2. Post-Login Routing
        if (isAuthorized){
            showTransactionsMenu();
        }
        else {
            System.out.println("Too many incorrect attempts. Program terminated for security reasons");
        }
    }
    
    // METHOD 1: Account Selection Menu
    public static void showTransactionsMenu(){
        
        System.out.println("1. Balance Inquiry");
        System.out.println("2. Deposit");
        System.out.println("3. Withdraw");
        System.out.println("4. Exit");
        System.out.print("Enter your choice (1, 2, 3, or 4): ");
        String transactionChoice=input.nextLine();
        
        switch (transactionChoice){
            case "1" -> {
                showBalanceInquiryMenu();
            }
            case "2" -> { 
                showDepositMenu();
            }
            case "3" -> {
                showWithdrawMenu();
            }
            case "4" -> {
                System.out.println("Thank you for your transaction with us..");
                System.exit(0);
            }
        }       
    }

    public static void showBalanceInquiryMenu() {
        System.out.println();
        System.out.println("Choose an account:");
        System.out.println("A. Savings");
        System.out.println("B. Checking");
        System.out.print("Enter your choice (A or B): ");
        String account=input.nextLine();
        
        if (account.equalsIgnoreCase("a")) {
            showSavingsBIMenu();
        } else if (account.equalsIgnoreCase("b")) {
            showCheckingBIMenu();
        } else {
            System.out.println("Invalid transaction, terminating program.");
        }
    }
        
    public static void showSavingsBIMenu(){
    
        System.out.println("\nYour current balance is Php " + savingAmt);
        confirmAnotherSession();
    }
    
    public static void showCheckingBIMenu() {
        
        System.out.println("\nYour current balance is Php " + checkingAmt);
        confirmAnotherSession();
    }

    public static void showDepositMenu() {
        
        System.out.println("Enter Amount: ");
    
    }

    public static void showWithdrawMenu() {
        System.out.println("Enter Amount: ");
    
    }

    public static void confirmAnotherSession() {
        
        System.out.println("Would you like to make another transaction? (Yes or No)");
        String choice=input.nextLine();
        
        if (choice.equalsIgnoreCase("Yes")){
            showTransactionsMenu();
        }
        else {
            System.out.println("Thank you for your transaction with us.");
            System.exit(0);
        }
    }
    
}
