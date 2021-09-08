# assignment2-sake

# Maneesh Sake

### Goa

My last vacation in india was in **Goa**.It is my favroite place.
**I went there with all my best friends and we enjoyed a lot.**

---
## Directions to Goa from Maryville

to travel to Goa from maryville
1. We need to take a taxi to international airport and book a flight ticket to goa
2. From kansas to delhi we need to take a immigration check and enter into to india 
    1. Follow rules properly
    2. Carry all required documents
3. From delhi to we have a direct flight to Goa 
4. Taxi will be available out side the airport in Goa 

# Things to carry to Goa for maximum enjoyment

* money 
    * cards 
    * liquid cash 
* Bike 
    * fuel tanks 
    * Air pump
* Beach
    * swimming Dress
    * diving suite

---

**[assignment2-sake](AboutMe.md)**

---

# Bawarchi Menu

Bawarchi is the place where we can find biryani. It is an indian delicious food. Here are the some of the items described below.

| Food/Beverage | Locaiton | Estimated Price |
| ------------- | -------- | --------------- |
| veg Biryani   | Overland Park | $12.99 |
| chicken Biryani | New Mexico | $9.83 |
| mutton Biryani | Los Angeles | $2.19 |
| Fish Biryani | New Haven | $4.56 |
| ice Cream   | New York | $4.00 |

# Study Quotes

>“Let us study things that are no more. It is necessary to understand them, if only to avoid them.”
― Victor Hugo, Les Misérables


>“The authority of those who teach is often an obstacle to those who want to learn.”
― Marcus Tullius Cicero

### Breadth-first search algorithm

> Breadth-first search (BFS) is an algorithm for searching a tree data structure for a node that satisfies a given property. It starts at the tree root and explores all nodes at the present depth prior to moving on to the nodes at the next depth level. Extra memory, usually a queue, is needed to keep track of the child nodes that were encountered but not yet explored.

link: <https://en.wikipedia.org/wiki/Breadth-first_search>

```
vector<vector<int>> adj;  // adjacency list representation
int n; // number of nodes
int s; // source vertex

queue<int> q;
vector<bool> used(n);
vector<int> d(n), p(n);

q.push(s);
used[s] = true;
p[s] = -1;
while (!q.empty()) {
    int v = q.front();
    q.pop();
    for (int u : adj[v]) {
        if (!used[u]) {
            used[u] = true;
            q.push(u);
            d[u] = d[v] + 1;
            p[u] = v;
        }
    }
}

if (!used[u]) {
    cout << "No path!";
} else {
    vector<int> path;
    for (int v = u; v != -1; v = p[v])
        path.push_back(v);
    reverse(path.begin(), path.end());
    cout << "Path: ";
    for (int v : path)
        cout << v << " ";
}

```
Link: <https://cp-algorithms.com/graph/breadth-first-search.html>
