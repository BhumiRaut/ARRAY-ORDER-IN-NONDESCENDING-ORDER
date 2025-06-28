# ARRAY-ORDER-IN-NONDESCENDING-ORDER
package pack1;
import java.util.stream.IntStream;

public class ArrayUtils {

    public static <T extends Comparable<T>> boolean isSorted(T[] array) {
        return IntStream.range(0, array.length - 1)
                .allMatch(i -> array[i].compareTo(array[i + 1]) <= 0);
    }

    public static void main(String[] args) {
        Integer[] numbers = {1, 2, 2, 3, 5};
        String[] words = {"apple", "banana", "cherry"};
        Integer[] unsorted = {4, 3, 5};

        System.out.println(isSorted(numbers));   
        System.out.println(isSorted(words));    
        System.out.println(isSorted(unsorted)); 
    }
}
