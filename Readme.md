# Deliverables
1. Implement classes for SinglyLinkedLists and Nodes. You can do this in ruby or js in one of the LinkedList files provided. 
>Note: If you are using ruby don't forget your attr_accessor

 <details>
      <summary>
        solution 
      </summary>
      <hr/>
      ```
      class Node
        attr_accessor :value, :next
      
        def initialize(value, next = nil)
          @value = value
          @next = next
        end
      end

      class LinkedList
        attr_accessor :head
      
        def initialize
          @head = nil
        end
      end
      ```
   
 </details>



2. Create a method on the Linked List class that appends a new node to the end of the list. 

```
# [c] -next-> nil
# head -> [a] -next-> [b] -next-> nil 

Expected output 
# head -> [a] -next-> [b] -next-> [c] -next-> nil


```


 <details>
      <summary>
        solution 
      </summary>
      <hr/>
      ```
      def append(node)
            if head.nil?
              self.head = node
              return
            end
        
            current = head
            while current.next
              current = current.next
            end
        
            current.next = node
          end
      ```
   
 </details>

3. You can add this print method to your class to test your append method.

```
def print
       current = @head

       while current
           puts current.value
           current = current.next
       end
end


```
