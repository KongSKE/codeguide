#Don,t repeat yourself
>Our first object oriented design principle is DRY, as name suggest DRY (don't repeat yourself) means don't write duplicate code,
instead use Abstraction to abstract common things in one place. If you have block of code in more than two place consider making it
a separate method, or if you use a hard-coded value more than one time make them public final constant. Benefit of this Object oriented 
design principle is in maintenance. It's important  not to abuse it, duplication is not for code, but for functionality . 
It means, if you used common code to validate OrderID and SSN it doesn’t mean they are same or they will remain same in future. 
By using common code for two different functionality or thing you closely couple them forever and when your OrderID changes its format ,
your SSN validation code will break. So beware of such coupling and just don’t combine anything which uses similar code but are not related.

```
package codeguide;
/**
 * Don't repeat yourself
 * @author Varit Assavavisidchai
 *
 */
//TODO delete duplicate code.
public class Bank {
	//name
	private String name;
	//id
	private String id;
  //money
  private double money;
	public (){
		this.name="name";
		this.id="ID";
    this.money=0;
	}
	//this method is default information.
	public void setBank(String name, String id , double money){
		this.name=name;
		this.id=id;
    this.money=money;
	}
	//this method for edit information.
	public void editBank(String name, String id, double money){
		this.name=name;
		this.id=id;
    this.money=money;
	}
	public String getMoney(){
		return name+id+money;
	}
}
```
So we must to delete duplicate code. this is editBamk method because it is the same as setBank method

Refernce: [Click here](http://javarevisited.blogspot.com/2012/03/10-object-oriented-design-principles.html)
