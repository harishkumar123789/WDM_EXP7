### EX7 Implementation of Link Analysis using HITS Algorithm

    return authority_scores, hub_scores


# 4-node adjacency matrix
# If Node i has a link to Node j, value = 1
adj_matrix = np.array([
    [0, 1, 1, 0],
    [0, 0, 1, 1],
    [0, 0, 0, 1],
    [1, 0, 1, 0]
])


# Run HITS algorithm
authority, hub = hits_algorithm(adj_matrix)


# Display results
print("HITS Algorithm Results")
print("----------------------")

for i in range(len(authority)):
    print(
        f"Node {i}: "
        f"Authority Score = {authority[i]:.4f}, "
        f"Hub Score = {hub[i]:.4f}"
    )


# Bar chart of Authority vs Hub scores
```
nodes = np.arange(len(authority))
bar_width = 0.35

plt.figure(figsize=(8, 6))

plt.bar(
    nodes - bar_width / 2,
    authority,
    bar_width,
    label='Authority',
    color='blue'
)

plt.bar(
    nodes + bar_width / 2,
    hub,
    bar_width,
    label='Hub',
    color='green'
)

plt.xlabel('Node')
plt.ylabel('Scores')
plt.title('Authority and Hub Scores for Each Node')

plt.xticks(
    nodes,
    [f'Node {i}' for i in range(len(authority))]
)

plt.legend()
plt.tight_layout()
plt.show()
```

### Output:

<img width="556" height="132" alt="image" src="https://github.com/user-attachments/assets/2a082042-1290-4150-8474-598f76a12c91" />

<img width="727" height="551" alt="image" src="https://github.com/user-attachments/assets/07554787-0332-4d94-88ed-d1ae3a19be39" />

### Result:
Therefore, Link Analysis using HITS Algorithm in Python is implemented and executed successfully.
