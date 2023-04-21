package stepdefinitions;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.edge.EdgeDriver;
import org.openqa.selenium.edge.EdgeOptions;

import io.cucumber.java.en.*;
import io.github.bonigarcia.wdm.WebDriverManager;
import page_object_model.loginpage;
import org.openqa.selenium.edgeoptions;

public class admin_demosteps {
	WebDriver driver=null;
	loginpage login;
	@Given("browser is open")
	public void browser_is_open() {
		WebDriverManager.edgedriver().setup();
		EdgeOptions options = new EdgeOptions();
		options.addArguments("--remote-allow-origins=*");
		//WebDriver driver = new ChromeDriver(options); 			
		WebDriverManager.edgedriver().setup();
		driver = new EdgeDriver(options);
	}

	@And("user is on login page")
	public void user_is_on_login_page() {
		driver.navigate().to("https://admin-demo.nopcommerce.com/login?ReturnUrl=%2FAdmin%2FCustomer%2FList");
	}

	@When("^user enters(.*)and(.*)$")
	public void user_enters_email_and_password(String Email, String password) {
		login=new loginpage(driver);
		login.enterEmail(Email);
        login.enterpassword(password);
	}

	@And("user clicks on login")
	public void user_clicks_on_login() {
		login.clicklogin();
	}


}
