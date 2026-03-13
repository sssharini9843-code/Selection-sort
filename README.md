def selection_sort(arr):
n = len(arr)
print(f"Original List: {arr}\n")

for i in range(n):
# Assume the first element of the unsorted part is the smallest
min_idx = i

# Check the rest of the unsorted part
for j in range(i + 1, n):
if arr[j] < arr[min_idx]:
min_idx = j

# Swap the found minimum element with the first element of the unsorted part
arr[i], arr[min_idx] = arr[min_idx], arr[i]

# Output the state of the list after each swap
print(f"Pass {i + 1} (Found min {arr[i]}): {arr}")

return arr

# --- Execution ---
data = [64, 25, 12, 22, 11]
sorted_data = selection_sort(data)
print("-" * 30)
print(f"Final Sorted List: {sorted_data}")


output:
Original List: [64, 25, 12, 22, 11]

Pass 1 (Found min 11): [11, 25, 12, 22, 64]
Pass 2 (Found min 12): [11, 12, 25, 22, 64]
Pass 3 (Found min 22): [11, 12, 22, 25, 64]
Pass 4 (Found min 25): [11, 12, 22, 25, 64]
Pass 5 (Found min 64): [11, 12, 22, 25, 64]
