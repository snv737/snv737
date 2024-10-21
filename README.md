graph = {'A': set(['B', 'C']),
         'B': set(['A', 'D', 'E']),
         'C': set(['A', 'F']),
         'D': set(['B']),
         'E': set(['B', 'F']),
         'F': set(['C', 'E'])
}

# Implement BFS logic
def bfs(start):
    queue = [start]
    levels = {}  # This dictionary keeps track of levels
    levels[start] = 0  # Depth of start node is 0
    visited = set([start])  # Initialize the visited set with the start node
    
    while queue:
        node = queue.pop(0)
        neighbours = graph[node]
        
        for neighbor in neighbours:
            if neighbor not in visited:
                queue.append(neighbor)
                visited.add(neighbor)
                levels[neighbor] = levels[node] + 1
    
    print(levels)  # Print graph levels
    return visited

print(bfs('A'))  # Print nodes visited by BFS

# For finding all paths from start to goal using BFS
def bfs_paths(graph, start, goal):
    queue = [(start, [start])]
    
    while queue:
        (vertex, path) = queue.pop(0)
        
        for next in graph[vertex] - set(path):
            if next == goal:
                yield path + [next]
            else:
                queue.append((next, path + [next]))

# List all paths from 'A' to 'F'
result = list(bfs_paths(graph, 'A', 'F'))
print(result)  # [['A', 'C', 'F'], ['A', 'B', 'E', 'F']]

# For finding the shortest path using BFS
def shortest_path(graph, start, goal):
    try:
        return next(bfs_paths(graph, start, goal))
    except StopIteration:
        return None

# Find the shortest path from 'A' to 'F'
result1 = shortest_path(graph, 'A', 'F')
print(result1)  # ['A', 'C', 'F']






def moveTower(height,fromPole, toPole, withPole):
    if height >= 1:
        moveTower(height-1,fromPole,withPole,toPole)
        moveDisk(fromPole,toPole)
        moveTower(height-1,withPole,toPole,fromPole)

def moveDisk(fp,tp):
    print("moving disk from",fp,"to",tp)
moveTower(3,"A","B","C")
