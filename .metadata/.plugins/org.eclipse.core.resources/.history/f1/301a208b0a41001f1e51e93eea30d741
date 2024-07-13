package stPackage;

import org.junit.Assert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import io.cucumber.java.en.Given;
import io.cucumber.java.en.Then;
import io.cucumber.java.en.When;

public class StepDefinition {
	
	WebDriver driver;
	
	@Given("user launch the application")
	public void user_launch_the_application() {
		
		
		 driver = new ChromeDriver();
		 driver.get("https://opensource-demo.orangehrmlive.com/web/index.php/auth/login");
		 driver.manage().window().maximize();
		 driver.getCurrentUrl();
		 driver.getTitle();
		 driver.close();
		
	   
	}

	@When("user provides valid username and password")
	public void user_provides_valid_username_and_password() {
		
		driver.findElement(By.name("username")).sendKeys("Admin");
		driver.findElement(By.name("password")).sendKeys("admin123");
	    
	}

	@When("user clicks the login button")
	public void user_clicks_the_login_button() {
		
		driver.findElement(By.xpath("//button[@type='submit']"));
	    
	}

	@Then("user validate the homescreen")
	public void user_validate_the_homescreen() {
		
		WebElement homePage = driver.findElement(By.xpath("//p[text()='Karan Singh']"));
		boolean verify = homePage.isDisplayed();
		Assert.assertTrue(verify);
	}



}
