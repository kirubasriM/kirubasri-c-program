int* intersect(int* nums1, int s1, int* nums2, int s2, int* r) {
    int hash1[1001] = {0};
    int hash2[1001] = {0};
    for (int i = 0; i < s1; i++) {
        hash1[nums1[i]]++;
    }
    for (int i = 0; i < s2; i++) {
        hash2[nums2[i]]++;
    }
    int count = 0;
    for (int i = 0; i <= 1000; i++) {
        count += hash1[i] < hash2[i] ? hash1[i] : hash2[i];
    }
    int* ans = malloc(count * sizeof(int));
    int index = 0;
    for (int i = 0; i <= 1000; i++) {
        for (int j = 0; j < (hash1[i] < hash2[i] ? hash1[i] : hash2[i]); j++) {
            ans[index++] = i;
        }
    }
    *r = count;

    return ans;
}
