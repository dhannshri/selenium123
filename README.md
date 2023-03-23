# selenium123
project
package testcase;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;

import io.github.bonigarcia.wdm.WebDriverManager;
//import io.github.bonigarcia.wdm.config.WebDriverManagerException;

//open as Browser

//System.setProperty("WebDriver.chrome.driver","\"C:\\Users\\Dhanashri\\Downloads\\chromedriver_win32 (1)\\chromedriver.exe\"");

public class MyFirstTest {
	public static void main(String[]args) {
		ChromeOptions co = new ChromeOptions();
		co.addArguments("--remote-allow-origins=*");
		//WebDriverManager.chromedriver().setup();
		WebDriver driver = new ChromeDriver(co);
		driver.get("https://www.zoho.com/");
		
		
		//System.out.println("Clicked successfully");
		driver.findElement(By.linkText("Sign in")).click();
		driver.findElement(By.id("//input[@id='login_id']")).sendKeys("dhanshridhekankar12@gmail.com");
		driver.findElement(By.xpath("//span[normalize-space()='Next']")).click();
		driver.findElement(By.xpath("//input[@id='password']")).sendKeys("dhanshridhekankar12@gmail.com");
		driver.findElement(By.xpath("//button[@id='nextbtn']//span[contains(text(),'Sign in')")).click();
		
	}

}
