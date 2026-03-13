def is_balanced(expression):
    stack = []
    mapping = {')': '(', '}': '{', ']': '['}
    
    for char in expression:
        if char in mapping.values():
            stack.append(char)
        elif char in mapping:
            if not stack or stack.pop() != mapping[char]:
                return False
    return not stack

# Execution
print(is_balanced("{ (a+b) * c }")) # Output: True
# -Kanaga-Data-structure-
