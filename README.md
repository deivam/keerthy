# keerthy
package automationFramework;

import org.openqa.selenium.support.ui.Select;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class FirstTestCase {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		WebDriver driver = new FirefoxDriver();
		driver.manage().window().maximize();
		driver.get("https://login.yahoo.com/config/login");
		driver.findElement(By.xpath(".//*[@id='login-signup']")).click();
		driver.findElement(By.xpath(".//*[@id='first-name']")).sendKeys("Keerthy prasad");
		driver.findElement(By.xpath(".//*[@id='last-name']")).sendKeys("Deivam");
		driver.findElement(By.xpath(".//*[@id='user-name']")).sendKeys("deivamkeerthy");
		driver.findElement(By.xpath(".//*[@id='password']")).sendKeys("9786997000");
		driver.findElement(By.xpath(".//*[@id='mobile']")).sendKeys("9786997000");		
		WebElement monthElement = driver.findElement(By.xpath(".//*[@id='month']"));
		Select monthSelect = new Select(monthElement);
		monthSelect.selectByValue("1");
		WebElement dayElement = driver.findElement(By.xpath(".//*[@id='day']"));
		Select daySelect = new Select(dayElement);
		daySelect.selectByValue("23");
		WebElement yearElement = driver.findElement(By.xpath(".//*[@id='year']"));
		Select yearSelect = new Select(yearElement);
		yearSelect.selectByValue("1993");
		WebElement genderRadioBtn = driver.findElement(By.xpath(".//*[@id='male']"));
		genderRadioBtn.click();
		driver.findElement(By.xpath(".//*[@id='mobile-rec']")).sendKeys("9842313399");
		driver.findElement(By.xpath(".//*[@id='relationship']")).sendKeys("brother");
		driver.findElement(By.xpath(".//*[@id='info-form']/div/div[9]/input")).click();		

	}

}
