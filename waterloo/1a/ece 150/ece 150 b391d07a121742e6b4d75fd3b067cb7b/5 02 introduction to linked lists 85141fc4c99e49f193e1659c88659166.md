# 5.02 introduction to linked lists

******nodes******

- each node of the linked list will contain its own value, as well as the pointer to the next value
- you just need to know the pointer to the first node, and all the rest follow

```cpp
class Node {
	public:
		double value;
		int next_value;
}
```

- to add things to the linked list, you have to constantly update the head
- we will dynamically allocate the nodes of the linked list so that we can continue to add to it so long as there is memory available