# Total-Cuts

def total_cuts(N, K, A):
    cuts = 0

    for i in range(1, N):
        max_left = max(A[:i])
        min_right = min(A[i:])

        if max_left + min_right >= K:
            cuts += 1

    return cuts

# Parse input
N, K = map(int, input().split())
A = list(map(int, input().split()))

# Calculate and print the total number of cuts
result = total_cuts(N, K, A)
print(result)
