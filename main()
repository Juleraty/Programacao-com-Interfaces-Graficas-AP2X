class Solution(object):
    '''
    Estamos criando um subconjunto de cada contêiner possível a partir da
    lista de alturas fornecida a nós. Portanto, a complexidade do tempo é O(N²)
    '''
    def maxArea(self, height):
        max_water = 0
        for left in range(len(height) - 1):
            for right in range(left + 1, len(height)):
                max_water = max(max_water, min(height[left], height[right]) * (right - left))
        return max_water


    def maxAreaOnePass(self, height):
        ''' Estamos analisando a lista apenas uma vez. 
        Portanto, a complexidade do tempo é O(N)'''
        left = 0
        right = len(height) - 1
        max_water = 0
        while (left < right):
            max_water = max(max_water, min(height[left], height[right]) * (right - left))
            if height[left] < height[right]:
                left += 1
            else:
                right -= 1
        return max_water



def main():
    test = [[1, 1],
            [1, 8, 6, 2, 5, 4, 8, 3, 7],
            [4, 3, 2, 1, 4],
            [],
            [1, 2, 1],
            [1, 2, 3, 4, 5, 6, 7, 8, 9]
            ]
    s = Solution()
    for t in test:
        r1 = s.maxArea(t)
        r2 = s.maxAreaOnePass(t)
        print("{} = {} = {}".format(t, r1, r2))


main()
