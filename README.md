# Ganzenbord
Eerste opdracht
import java.util.Random;
import java.util.Scanner;

public class GanzenbordLastig {

	public static void main(String[] args) {
		System.out.println("Speler 1, je staat op Start. Gooi je dobbelsteen (g):");
		System.out.println("Speler 2, je staat op Start. Gooi je dobbelsteen (g):");
		int plaats1 = 0;
		int plaats2 = 0;
		int worp1;
		int worp2;
		int overslaan1 = 0;
		int overslaan2 = 0;
		while (plaats1 < 63 && plaats2 < 63) {
			Scanner zoeken1 = new Scanner(System.in);
			String ingave1 = zoeken1.nextLine();
			Scanner zoeken2 = new Scanner(System.in);
			String ingave2 = zoeken2.nextLine();
			if (overslaan1 != 0) {
				System.out.println("Deze beurt overslaan.");
				overslaan1--;
			}
			else {
		switch(ingave1){
			case "g":
				worp1 = dobbelen() + 1;
				plaats1 = plaats1 + worp1;
				switch(plaats1) { 
				case 6:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ". Ga verder naar 12.");
					plaats1 = 12;
					break;
				case 10:
					System.out.print("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ".");
					plaats1 = plaats1 + worp1;
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;
				case 19:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ". Volgende beurt overslaan.");
					overslaan1++;
					break;
				case 20:
					System.out.print("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ".");
					plaats1 = plaats1 + worp1;
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;
				case 30:
					System.out.print("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ".");
					plaats1 = plaats1 + worp1;
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;
				case 31:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + " (put). Blijf hier tot een andere speler deze plek passeert.");
					if(plaats2 < 31) {
						overslaan1++;
					}
					else {
						overslaan1 = 0;
					}
					break;
				case 40:
					System.out.print("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ".");
					plaats1 = plaats1 + worp1;
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;
				case 42:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + " (doolhof). Ga terug naar 39.");
					plaats1 = 39;
					break;
				case 50:
					System.out.print("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ".");
					plaats1 = plaats1 + worp1;
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;
				case 52: 
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ". Gevangenis! Sla 3 beurten over.");
					overslaan1 = overslaan1 + 3;
					break;
				case 58:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + " (dood). Helaas terug naar de start! Gooi je dobbelsteen (g).");
					plaats1 = 0;
					break;
				case 60:
					System.out.print("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ".");
					plaats1 = plaats1 + worp1;
					switch(plaats1) {
					case 61:
						System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;	
					case 62:
						System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gooi je dobbelsteen (g).");
					break;
					case 63:
						System.out.println(" Bonus stapjes! Je staat op plaats " + plaats1 + ". Gefeliciteerd, je hebt gewonnen!");
					break;
					case 64:
						plaats1 = 62;
						System.out.println(" Bonus stapjes! Helaas 1 te veel. Je staat op plaats " + plaats1 + ".");
						break;
					case 65:
						plaats1 = 61;
						System.out.println(" Bonus stapjes! Helaas 2 te veel. Je staat op plaats " + plaats1 + ".");
						break;
					case 66:
						plaats1 = 60;
						System.out.println(" Bonus stapjes! Helaas 3 te veel. Je staat op plaats " + plaats1 + ".");
						break;
					}
					break;
				case 63:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ". Gefeliciteerd, je hebt gewonnen!");
				break;
				case 64:
					plaats1 = 62;
					System.out.println("Je hebt " + worp1 + " gegooid, dat is 1 te veel. Je staat op plaats " + plaats1 + ".");
					break;
				case 65:
					plaats1 = 61;
					System.out.println("Je hebt " + worp1 + " gegooid, dat is 2 te veel. Je staat op plaats " + plaats1 + ".");
					break;
				case 66:
					plaats1 = 60;
					System.out.println("Je hebt " + worp1 + " gegooid, dat is 3 te veel. Je staat op plaats " + plaats1 + ".");
					break;
				case 67:
					plaats1 = 59;
					System.out.println("Je hebt " + worp1 + " gegooid, dat is 4 te veel. Je staat op plaats " + plaats1 + ".");
					break;
				case 68:
					plaats1 = 58;
					System.out.println("Je hebt " + worp1 + " gegooid, dat is 5 te veel. Je staat op plaats " + plaats1 + ".");
					break;
				default:
					System.out.println("Je hebt " + worp1 + " gegooid, je staat op plaats " + plaats1 + ". Niks aan de hand. Gooi je dobbelsteen (g).");
				}
				break;
			default:
				System.out.println("Verkeerde keuze. Gooi je dobbelsteen (g):");
				}
			}
			if (overslaan2 != 0) {
				System.out.println("Deze beurt overslaan.");
				overslaan2--;
			}
			else {
	switch(ingave2){
		case "g":
			worp2 = dobbelen() + 1;
			plaats2 = plaats2 + worp2;
			
			switch(plaats2) { 
			case 6:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ". Ga verder naar 12.");
				plaats2 = 12;
				break;
			case 10:
				System.out.print("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ".");
				plaats2 = plaats2 + worp2;
				System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;
			case 19:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ". Volgende beurt overslaan.");
				overslaan2++;
				break;
			case 20:
				System.out.print("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ".");
				plaats2 = plaats2 + worp2;
				System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;
			case 30:
				System.out.print("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ".");
				plaats2 = plaats2 + worp2;
				System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;
			case 31:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + " (put). Blijf hier tot een andere speler deze plek passeert.");
				if(plaats1 < 31) {
					overslaan2++;
				}
				else {
					overslaan2 = 0;
				}
				break;
			case 40:
				System.out.print("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ".");
				plaats2 = plaats2 + worp2;
				System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;
			case 42:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + " (doolhof). Ga terug naar 39.");
				plaats2 = 39;
				break;
			case 50:
				System.out.print("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ".");
				plaats2 = plaats2 + worp2;
				System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;
			case 52: 
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ". Gevangenis! Sla 3 beurten over.");
				overslaan2 = overslaan2 + 3;
				break;
			case 58:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + " (dood). Helaas terug naar de start! Gooi je dobbelsteen (g).");
				plaats2 = 0;
				break;
			case 60:
				System.out.print("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ".");
				plaats2 = plaats2 + worp2;
				switch(plaats2) {
				case 61:
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;	
				case 62:
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gooi je dobbelsteen (g).");
				break;
				case 63:
					System.out.println(" Bonus stapjes! Je staat op plaats " + plaats2 + ". Gefeliciteerd, je hebt gewonnen!");
				break;
				case 64:
					plaats2 = 62;
					System.out.println(" Bonus stapjes! Helaas 1 te veel. Je staat op plaats " + plaats2 + ".");
					break;
				case 65:
					plaats2 = 61;
					System.out.println(" Bonus stapjes! Helaas 2 te veel. Je staat op plaats " + plaats2 + ".");
					break;
				case 66:
					plaats2 = 60;
					System.out.println(" Bonus stapjes! Helaas 3 te veel. Je staat op plaats " + plaats2 + ".");
					break;
				}
				break;
			case 63:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ". Gefeliciteerd, je hebt gewonnen!");
			break;
			case 64:
				plaats2 = 62;
				System.out.println("Je hebt " + worp2 + " gegooid, dat is 1 te veel. Je staat op plaats " + plaats2 + ".");
				break;
			case 65:
				plaats2 = 61;
				System.out.println("Je hebt " + worp2 + " gegooid, dat is 2 te veel. Je staat op plaats " + plaats2 + ".");
				break;
			case 66:
				plaats2 = 60;
				System.out.println("Je hebt " + worp2 + " gegooid, dat is 3 te veel. Je staat op plaats " + plaats2 + ".");
				break;
			case 67:
				plaats2 = 59;
				System.out.println("Je hebt " + worp2 + " gegooid, dat is 4 te veel. Je staat op plaats " + plaats2 + ".");
				break;
			case 68:
				plaats2 = 58;
				System.out.println("Je hebt " + worp2 + " gegooid, dat is 5 te veel. Je staat op plaats " + plaats2 + ".");
				break;
			default:
				System.out.println("Je hebt " + worp2 + " gegooid, je staat op plaats " + plaats2 + ". Niks aan de hand. Gooi je dobbelsteen (g).");
			}
			break;
		default:
			System.out.println("Verkeerde keuze. Gooi je dobbelsteen (g):");
			}
			}
		}
		}

	static int dobbelen(){
		Random random = new Random();
		return random.nextInt(6);
	}
	
}
