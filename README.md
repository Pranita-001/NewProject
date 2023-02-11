# NewProject
package com.google;
import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class Google1 {
	public static void main(String[] args){
		// Set Driver path
		System.setProperty("webdriver.chrome.driver","D:/JAVA BY KIRAN/Selenium/chromedriver.exe");
		WebDriver driver=new ChromeDriver();
		//open google
		driver.get("https://www.google.com");
		driver.manage().timeouts().implicitlyWait(15, TimeUnit.SECONDS);
		//enter brovitech llp solutions pune  in search box
		driver.findElement(By.name("q")).sendKeys("brovitech llp solutions pune");
		driver.findElement(By.xpath("/html/body/div[1]/div[3]/form/div[1]/div[1]/div[2]/div[2]/div[2]/div[1]/div/ul/li[1]/div/div[2]/div[1]/span")).click();
		driver.quit();
}

}
