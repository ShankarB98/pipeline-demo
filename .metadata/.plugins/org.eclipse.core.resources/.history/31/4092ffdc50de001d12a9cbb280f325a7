package stepdefinitions;

import org.junit.Assert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.edge.EdgeDriver;
import org.openqa.selenium.edge.EdgeOptions;

import io.cucumber.java.en.*;
import io.github.bonigarcia.wdm.WebDriverManager;
import page_object_model.loginpage;

public class AdminSteps {
	WebDriver driver=null;
	loginpage login;
	@Given("User Launch Chrome browser")
	public void user_launch_chrome_browser() {
		EdgeOptions options = new EdgeOptions();
		options.addArguments("--remote-allow-origins=*");
		//WebDriver driver = new ChromeDriver(options); 			
		WebDriverManager.edgedriver().setup();
		driver = new EdgeDriver(options);

	}
	@When("User opens URL {string}")
	public void user_opens_U_rl(String url){
	driver.get(url);

	}
	@When("User enters Email as {string} and Password as {string}")
	public void user_enters_email_as_and_password_as(String Email, String Password) {
		login=new loginpage(driver);
		login.enterEmail(Email);
        login.enterpassword(Password);
	}
	@When("Click on Login")
	public void click_on_login() {
		login.clicklogin();
	}
	@Then("Page Title should be {string}")
	public void page_title_should_be(String title) {
	if(driver.getPageSource().contains("Login was unsuccessful")){
	driver.close();
	Assert.assertTrue(false);
	}
	else{
	Assert.assertEquals(title,driver.getTitle());
	}
	
	@When("User click on Log out link")
	public void user_click_on_log_out_link()throws Exception {
		login.clickLogout();
	Thread.sleep(3000);

	}
	@Then("close browser")
	public void close_browser() {
	driver.close();
}
	@Then("User can view Dashboard")
	public void user_can_view_dashboard() {
	login=new loginpage(driver);
	Assert.assertEquals("Dashboard / nopCommerce administration",login.setPageTitle());
	}
	@When("User click on customers Menu")
	public void user_click_on_customers_menu() {

	login.clickOnCustomersmenu();

	}
	@When("click on customers Menu Item")
	public void click_on_customers_menu_item() {
	login.clickonLnkCustomers_menuitem();
	}
	@When("click on Add new button")
	public void click_on_add_new_button() {
	login.clickonAddnew();

	}
	@Then("User can view Add new customer page")
	public void user_can_view_add_new_customer_page() {
	Assert.assertEquals("Add a new customer / nopCommerce administration",login.setPageTitle());

	}
	
	@When("User enter customer info")
	public void user_enter_customer_info() throws InterruptedException {
	String email=toString()+"@gmail.com";
	login.setmail("abc@gmail.com");
	//login.setPassword("test123");
	login.setcustomerRoles("Guest");

	login.setManagerOfVendor("Vendor 2");
	login.setGender("Female");
	login.setFirstName("Usha");
	login.setLastName("rani");
	login.setDob("08/24/1990");
	login.setCompanyName("Kairos");
	login.setAdminContent("Hello");


	}
	@When("click on Save button")
	public void click_on_save_button() {
	login.clickonSave();

	}
	@Then("User can view confirmation message {string}")
	public void user_can_view_confirmation_message(String string) {
	Assert.assertTrue(driver.findElement(By.tagName("body")).getText().contains("The new customer has been added successfully"));

	

	}
}
