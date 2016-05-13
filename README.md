package array;

import java.util.Arrays;

public class MovingZeros {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		int arr[] = {109090,2,0,5,0,0,10,8,0,-20000,0,4,0};
		System.out.println("Before move:"+Arrays.toString(arr));
		zeromove(arr);
	}

	
	private static void zeromove(int[] arr){
		
		int start =0;
		int end = arr.length-1;
		
		while(start < end){
			if(arr[start] == 0 && arr[end] != 0){
				int temp = arr[start];
				arr[start++] = arr[end];
				arr[end--] = temp;
				
			} 
			if(arr[start] != 0){
				start++;
			} 
			if (arr[end] == 0){
				end--;
			}
		}
			
		System.out.println("After move:"+Arrays.toString(arr));
	}
}
