# Selenium-maven
Selenium Java Test Using maven

SETUP SELENIUM DEVELOPMENT ENVIRONMENT
download selenium server and add it to the project library build path as an external jar file

MAVEN DEPENDENCY
Maven helps in managing your project dependencies such as jdk, junit, selenium server and even the browser drivers. When new versions of the
dependencies are released you do not have to worry about upgrading, maven does it for you. Maven already comes with some IDE like Eclipse
but if you want to run your products outside the IDE, you have to download Maven, save it in a dedicated folde in C-drive and setup
environment variable for it:- MAVEN_HOME(path to maven, excluding bin) and Path Variable(path to maven, including bin). check the version
in command line to confirm success. remember to close and reopen the cmd if it is already open. Maven assists teams to synchronize.
POM.xml is used tomanage dependencies in maven projects.

Add selenium server to the pom: 
go to https://www.selenium.dev/downloads/ 
click mvn repository, java, click the version and copy the complete set of dependency tags and values
paste within <dependencies> tags
if you want ot remove the dependency, simply remove the tags and save
ctrl + shift + f can be used to format the codes

Example:



import org.openqa.selenium.By;
import org.openqa.selenium.chrome.*;


public class Maven_Example {

	public static void main(String[] args) {
		ChromeDriver driver = new ChromeDriver();

		driver.get("https://www.ebay.com");
		driver.manage().window().maximize();
		driver.findElement(By.xpath("//*[@id=\"gh-ac\"]")).sendKeys("mobile");
		driver.findElement(By.xpath("//*[@id=\"gh-btn\"]")).click();
		driver.close();
	}

}
