import re

import string

text = """România se confruntă cu o creștere semnificativă a prețurilor la energie, 

iar autoritățile analizează noi măsuri pentru protejarea consumatorilor casnici."""

middle = len(text) // 2

first_half = text[:middle]

second_half = text[middle:]l

first_half = first_half.upper().strip()



second_half = second_half[::-1]

if len(second_half) > 0:

    second_half = second_half[0].upper() + second_half[1:]

second_half = re.sub(r'[.,!?]', '', second_half)

combined_text = first_half + " " + second_half

print("=== TEXT FINAL ===")

print(combined_text)
