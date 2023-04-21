package page_object_model;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;

public class loginpage {
	WebDriver driver;
	By txt_Email=By.id("Email");
	By txt_password=By.id("Password");
	By btn_login=By.xpath("//*[text()='Log in']");
	By btn_Customers=By.id("Customers");
	By btn_Addnew=By.id("Addnew");
	By btn_Save=By.id("Save");
	By txt_email=By.id("email");
	By txt_customerRoles=By.id("customerRoles");
	By txtEmail = By.xpath("//input[@id='Email']");
	
	By btn_logout=By.id("logout");
	
	By lnkCustomers_menu = By.xpath("//i[@class='nav-icon far fa-user']");
	By lnkCustomers_menuitem = By.xpath("//li[@class='nav-item has-treeview menu-open']//ul[@class='nav nav-treeview']//p[contains(text(),'Customers')]");
	//By.xpath("//a[@class='nav-link active']//i[@class='nav-icon far fa-dot-circle']");
	By btnAddnew = By.xpath("//body/div[3]/div[1]/form[1]/div[1]/div[1]/a[1]");
	By txtEmail1 = By.xpath("//input[@id='Email']");
	By txtPassword = By.xpath("//input[@id='Password']");

	By txtcustomerRoles = By.xpath("//div[@class='k-multiselect-wrap k-floatwrap']");

	By listitemAdministrators = By.xpath("//li[contains(text(),'Administrators')]");
	By listitemRegistered = By.xpath("//li[contains(text(),'Registered')]");
	By listitemGuests = By.xpath("//li[contains(text(),'Guests')]");
	By listitemvendors = By.xpath("//li[contains(text(),'Vendors')]");

	By drpmgrofvendor = By.xpath("//*[@id='VendorId']");
	By rdMaleGender = By.id("Gender_Male");
	By rdFemaleGender = By.id("Gender_Female");

	By txtFirstName = By.xpath("//input[@id='FirstName']");
	By txtLastName = By.xpath("//input[@id='LastName']");

	By txtDob = By.xpath("//input[@id='DateOfBirth']");

	By txtCompanyName = By.xpath("//input[@id='Company']");

	By txtAdminContent = By.xpath("//textarea[@id='AdminComment']");

	By btnSave = By.xpath("//button[@name='save']");

	
	public loginpage(WebDriver driver) {
		this.driver=driver;
		
	}
	
	
	public void enterEmail(String Email)
	{
		driver.findElement(txt_Email).clear();
		driver.findElement(txt_Email).sendKeys(Email);
	}
	public void enterpassword(String password)
	{
		driver.findElement(txt_password).clear();
		driver.findElement(txt_password).sendKeys(password);
	}
	public void clicklogin() {
		driver.findElement(btn_login).click();
	}
	public void clickOnCustomersmenu()
	{
		driver.findElement(txt_customerRoles).click();
	}
	public void clickonAddnew()
	{
		driver.findElement(btn_Addnew).click();
	}
	public void clickLogout()
	{
		driver.findElement(btn_logout).click();
		}
	public void clickonSave()
	{
		driver.findElement(btn_Save).click();
	}
	public void setmail(String email) {
		driver.findElement(txtEmail).sendKeys(email);
	}
	public void setEmail()
	{
		//driver.findElement(txt_email).sendkeys(email);
		driver.findElement(txt_password).sendKeys("test123");
		driver.findElement(txt_customerRoles).sendKeys("guest");

		
		
		
	}
	public void clickOnCustomersmenu1() {
		driver.findElement(lnkCustomers_menu).click();
		}

		public void clickonLnkCustomers_menuitem1() {
		driver.findElement(lnkCustomers_menuitem).click();
		}

		public void clickonAddnew1() {
		driver.findElement(btnAddnew).click(); }

		public void setEmail(String email) {
		driver.findElement(txtEmail).sendKeys(email);
		}

		public void setPassword(String password) {
		driver.findElement(txtPassword).sendKeys(password);
		}

		public void setcustomerRoles(String role) throws InterruptedException {
		if (!role.equals("vendors")) {
		driver.findElement(By.xpath("//*[@id=\"SelectedCustomerRoleIds_taglist\"]/li/span[2]")).click();
		}
		driver.findElement(txtcustomerRoles).click();
		WebElement listitem;

		Thread.sleep(3000);
		if (role.equals("Administrators")) {
		listitem = driver.findElement(listitemAdministrators);
		} else if (role.equals("Guests")) {
		listitem = driver.findElement(listitemGuests);
		} else if (role.equals("Registered")) {
		listitem = driver.findElement(listitemRegistered);
		} else if (role.equals("Vendors")) {
		listitem = driver.findElement(listitemvendors);
		} else {
		listitem = driver.findElement(listitemGuests);

		}
		JavascriptExecutor js = (JavascriptExecutor) driver;
		js.executeScript("arguments[0].click();", listitem);
		}

		public void setManagerOfVendor(String value) {
		Select drp = new Select(driver.findElement(drpmgrofvendor));
		drp.selectByVisibleText(value);
		}

		public void setGender(String gender) {
		if (gender.equals("Male")) {
		driver.findElement(rdMaleGender).click();
		} else if (gender.equals("Female")) {
		driver.findElement(rdFemaleGender).click();
		} else {
		driver.findElement(rdMaleGender).click();
		}
		}

		public void setFirstName(String fname) {
		driver.findElement(txtFirstName).sendKeys(fname);
		}

		public void setLastName(String lname) {
		driver.findElement(txtLastName).sendKeys(lname);
		}

		public void setDob(String dob) {
		driver.findElement(txtDob).sendKeys(dob);
		}

		public void setCompanyName(String cmpny) {
		driver.findElement(txtCompanyName).sendKeys(cmpny);
		}

		public void setAdminContent(String cmnt) {
		driver.findElement(txtAdminContent).sendKeys(cmnt);
		}

		public void clickonSave1() {
		driver.findElement(btnSave).click();
		}
		}



//	private WebElement btn_Addnew() {
//		// TODO Auto-generated method stub
//		return null;
//	}
//	//public void checkLogOutsDisplayed()
//	{
		//driver.findElement(btn_logout).isDisplayed();


	public Object setPageTitle() {
		// TODO Auto-generated method stub
		return null;
	}


	public Object setPageTitle1() {
		// TODO Auto-generated method stub
		return null;
	}


	public void clickonLnkCustomers_menuitem() {
		// TODO Auto-generated method stub
		
	}
	}
		
	





