package user;

public class User {
	private String name;
	private Integer age;

	// 无参构造
	public User() {
		super();
	}

	public User(String name, Integer age) {
		super();
		this.name = name;
		this.age = age;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public Integer getAge() {
		return age;
	}

	public void setAge(Integer age) {
		this.age = age;
	}

	@Override
	public int hashCode() {
		final int prime = 31;
		int result = 1;
		result = prime * result + ((age == null) ? 0 : age.hashCode());
		result = prime * result + ((name == null) ? 0 : name.hashCode());
		return result;
	}

	@Override
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (getClass() != obj.getClass())
			return false;
		User other = (User) obj;
		if (age == null) {
			if (other.age != null)
				return false;
		} else if (!age.equals(other.age))
			return false;
		if (name == null) {
			if (other.name != null)
				return false;
		} else if (!name.equals(other.name))
			return false;
		return true;
	}

	@Override
	public String toString() {
		return "User [name=" + name + ", age=" + age + "]";
	}
}





package test;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;
import java.util.List;

import user.User;

public class Tset01 {

	public static void main(String[] args) {
		Comparator<User> com = new Comparator<User>() {

			@Override
			public int compare(User o1, User o2) {
				return o1.getAge()-o2.getAge();
			}
			
		};
		List<User> userlist = new ArrayList<User>();
		
		for(int i=0;i<10;i++){
			userlist.add(new User("user0"+(i+1),(int)(Math.random()*43)+18));
		}
		Collections.sort(userlist,com);
		for(User user:userlist){
			System.out.println(user);
		}
		
	}
}

