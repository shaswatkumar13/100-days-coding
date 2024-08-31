class Solution {
    // Function to find three numbers such that arr[smaller[i]] < arr[i] <
    // arr[greater[i]]
  public List<Integer> find3Numbers(int[] arr) {
        int n = arr.length;
        List<Integer> result = new ArrayList<>();
        Stack<int[]> st = new Stack<>();
        int[] parent = new int[n];
        int[] parent2 = new int[n];

        Arrays.fill(parent, -1);
        Arrays.fill(parent2, -1);
        st.push(new int[]{arr[n - 1], n - 1});
        for (int i = n - 2; i >= 0; i--) {
            while (!st.isEmpty() && st.peek()[0] <= arr[i]) {
                st.pop();
            }
            if (!st.isEmpty()) {
                parent[i] = st.peek()[1];
            }
            st.push(new int[]{arr[i], i});
        }

        st.clear();
        st.push(new int[]{arr[0], 0});
        for (int i = 1; i < n; i++) {
            while (!st.isEmpty() && st.peek()[0] >= arr[i]) {
                st.pop();
            }
            if (!st.isEmpty()) {
                parent2[i] = st.peek()[1];
            }
            st.push(new int[]{arr[i], i});
        }

        for (int i = 0; i < n; i++) {
            if (parent2[i] != -1 && parent[i] != -1) {
                result.add(arr[parent2[i]]);
                result.add(arr[i]);
                result.add(arr[parent[i]]);
                break;
            }
        }
        return result;
    }
}
