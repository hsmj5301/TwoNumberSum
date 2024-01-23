/*Initially, I implemented the solution for the "Two Number Sum" problem using a nested loop. This approach involved
        iterating through each element of the array and, for each element, iterating again through the rest of the array
        looking for a complementary number that, when added together, would equal the target sum. While straightforward,
        this method proved to be inefficient with a time complexity of O(n2)O(n2), especially as the size of the input
        array grew larger.
        Realizing the limitations of this approach, I transitioned to using a hash set. The motivation behind this was
        to capitalize on the hash set's average O(1)O(1) time complexity for both insertion and lookup operations, which
        would allow me to significantly reduce the overall time complexity of the solution to O(n)O(n). Here's how it works:
        As I iterate through the array, I calculate what the potential matching number (complement) would need to be
        for each element to reach the target sum. The complement is simply the target sum minus the current element.
        I then check if this complement is already present in the hash set. If it is, that means I've already encountered
        the number that, when added to the current element, sums up to the target sum.
        If the complement is not in the hash set, I add the current element to the set and continue iterating through
        the array. This ensures that each element is checked only once against all previously seen elements, which is
        much more efficient than checking against all elements as in the nested loop approach.
        The hash set also inherently takes care of the requirement that we cannot add a number to itself to reach the
        target sum, as it only stores unique numbers and checks for a distinct complement.
        By adopting this new approach, I was able to improve the performance of my solution, which is especially
        noticeable with large input arrays. This optimization is a classic example of a space-time trade-off, where
        a bit of extra space used by the hash set results in a dramatic increase in time efficiency. The change to using
        a hash set also made the code simpler and more readable, eliminating the need for complex nested loops and making
        it easier to maintain and understand.
        Overall, the shift from a nested loop to a hash set was a strategic decision to enhance the algorithm's
        efficiency, capitalizing on the strengths of hash set operations to produce a scalable and performant solution. */


        
