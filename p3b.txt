# Minimum Spanning Tree (MST) using Greedy Algorithm – Prim’s Algorithm

## Simple C++ Code

```cpp
#include <iostream>
using namespace std;

int main()
{
    int cost[4][4] = {
        {0, 10, 15, 20},
        {10, 0, 35, 25},
        {15, 35, 0, 30},
        {20, 25, 30, 0}
    };

    bool visited[4] = {false};

    visited[0] = true;

    int edges = 0;

    cout << "Edges in MST:\n";

    while (edges < 3)
    {
        int min = 999;
        int x = 0, y = 0;

        for (int i = 0; i < 4; i++)
        {
            if (visited[i])
            {
                for (int j = 0; j < 4; j++)
                {
                    if (!visited[j] && cost[i][j])
                    {
                        if (cost[i][j] < min)
                        {
                            min = cost[i][j];
                            x = i;
                            y = j;
                        }
                    }
                }
            }
        }

        cout << x << " - " << y << " : " << cost[x][y] << endl;

        visited[y] = true;
        edges++;
    }

    return 0;
}
```

---

# Output

```text
Edges in MST:
0 - 1 : 10
0 - 2 : 15
0 - 3 : 20
```

---

# Line by Line Explanation

## Header File

```cpp
#include <iostream>
```

Used for input and output.

```cpp
using namespace std;
```

Uses standard namespace.

---

# Cost Matrix

```cpp
int cost[4][4]
```

Stores graph edge weights.

Example:

* cost[0][1] = 10
* cost[1][2] = 35

---

# Visited Array

```cpp
bool visited[4] = {false};
```

Checks visited nodes.

---

# Start Node

```cpp
visited[0] = true;
```

Starts from node 0.

---

# Edge Counter

```cpp
int edges = 0;
```

Counts selected edges.

---

# While Loop

```cpp
while (edges < 3)
```

Runs until MST completed.

For 4 nodes:

* MST needs 3 edges

---

# Minimum Value

```cpp
int min = 999;
```

Stores minimum edge weight.

---

# Outer Loop

```cpp
for (int i = 0; i < 4; i++)
```

Checks visited nodes.

---

# Inner Loop

```cpp
for (int j = 0; j < 4; j++)
```

Checks connected nodes.

---

# Edge Condition

```cpp
if (!visited[j] && cost[i][j])
```

Checks:

* node not visited
* edge exists

---

# Find Minimum Edge

```cpp
if (cost[i][j] < min)
```

Finds smallest edge.

```cpp
min = cost[i][j];
```

Updates minimum value.

```cpp
x = i;
y = j;
```

Stores edge nodes.

---

# Print MST Edge

```cpp
cout << x << " - " << y;
```

Prints selected edge.

---

# Mark Node Visited

```cpp
visited[y] = true;
```

Marks node as visited.

---

# Increase Edge Count

```cpp
edges++;
```

Counts selected edge.

---

# Simple Theory

## Minimum Spanning Tree (MST)

* Connects all vertices
* Minimum total cost
* No cycles

## Prim’s Algorithm

Greedy algorithm that:

1. Starts from one node
2. Selects minimum edge
3. Adds new node
4. Repeats until all nodes connected

---

# Time Complexity

```text
O(V²)
```
