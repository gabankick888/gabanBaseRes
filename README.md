# gabanBaseRes
learn and try commint to base builder
gabanBaseRes/
├── swap/          
├── sorting/       
├── search/         
└── utils/          
# bubble_sort.py

def bubble_sort(arr):
    n = len(arr)

    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]   # ← swap!

    return arr


data = [64, 34, 25, 12, 22, 11, 90]
print(f"Sebelum: {data}")

hasil = bubble_sort(data)
print(f"Sesudah:  {hasil}")

# Output:
# Sebelum: [64, 34, 25, 12, 22, 11, 90]
# Sesudah:  [11, 12, 22, 25, 34, 64, 90]

# linear_search.py

def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i   # kembalikan index jika ketemu
    return -1          # kembalikan -1 jika tidak ada


data = [5, 3, 8, 1, 9, 2, 7]
target = 9

index = linear_search(data, target)

if index != -1:
    print(f"Nilai {target} ditemukan di index {index}")
else:
    print(f"Nilai {target} tidak ditemukan")

# Output: Nilai 9 ditemukan di index 4
