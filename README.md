# backend-interview
package test;

public class Test {
	public static void main(String[] args) {
		int [] a={9,-56,45,-85,48,-49,65,-64,67};
		sort(a);
	}
	public static void sort(int[] a){
		int temp=0;
		for (int i = 0; i < a.length-1; ++i) {
			for (int j = 0; j < a.length-i-1; ++j) {
				if (a[j+1]<a[j]) {
					temp=a[j];
					a[j]=a[j+1];
					a[j+1]=temp;
				}
			}
		}
		System.out.println("冒泡排序的结果：");
		for (int i = 0; i < a.length; i++) {
			System.out.print(a[i]+"   ");
		}
	}

}
