import java.util.Scanner;
class Account {
	String custName;
	String accNum;
	double deposit;
	double balance;
	double withdrawalAmt;

	void getd() {
	Scanner sc = new Scanner(System.in);
	System.out.println("Enter the customer name");
	custName = sc.nextLine();
	System.out.println("Enter the customer account number");
	accNum = sc.nextLine();
	System.out.println("Enter the deposit amount");
	deposit = sc.nextDouble();
	balance=deposit;
	System.out.println();

	}
	void putd() {
	System.out.println("Customer name: "+custName);
	System.out.println("Account number: "+accNum);
	System.out.println();
	}
}

class CurAcct extends Account {
	void balanceCheck() {
		if (balance<=10000) {
			System.out.println("You have less than minimum balance!");
			balance-=1000;
		}
	}
	void calcDisplayBalance() {
		System.out.println("Current account details");
		putd();
		System.out.println("Enter amount to be withdrawn");
		Scanner sc = new Scanner(System.in);
		withdrawalAmt = sc.nextDouble();
		balance-=withdrawalAmt;
		balanceCheck();
		System.out.println("Balance (after checking with minimum balance): "+balance);
		System.out.println();
	}
}

class SavAcct extends Account {
	void interestCalc() {
	balance=balance+(0.07*balance);
	}
	void calcDisplayBalance() {
	Scanner sc = new Scanner(System.in);
	System.out.println("Savings account details");
	putd();
	System.out.println("Enter amount to be withdrawn");
	withdrawalAmt = sc.nextDouble();
	balance-=withdrawalAmt;
	System.out.println("Balance before addition of compound interest: "+balance);
	interestCalc();
	System.out.println("Balance after compound interest addition: "+balance);
	System.out.println();
	}
}

class Bank {
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
		String accType;
		System.out.println("Enter the type of account (Savings account or Current account)");
		accType = sc.nextLine();
		if (accType.equals("Savings account")) {
			SavAcct sacc = new SavAcct();
			sacc.getd();
			sacc.calcDisplayBalance();
		}
		else if (accType.equals("Current account")) {
			CurAcct cacc = new CurAcct();
			cacc.getd();
			cacc.calcDisplayBalance();
		}
		else {
			System.out.println("Enter a valid account type");
		}
	}
}
