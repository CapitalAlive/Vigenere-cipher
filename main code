from string import ascii_lowercase as lc

key_length = int(input().replace("> ", ""))
hint = input().replace(" ", "").replace(">", "")
encoded_hint = input().replace(" ", "").replace(">", "")
encoded_message = input().replace(" ", "").replace(">", "")
keyword = []
final_message = ""

for n in range(key_length):
    keyword.append(lc.index(hint[n]) - lc.index(encoded_hint[n]))

keyword_index = 0
for letter in encoded_message:
    if keyword_index == len(keyword):
        keyword_index = 0
    index_to_append = lc.index(letter) + keyword[keyword_index]
    if index_to_append > 25:
        index_to_append -= 26
    final_message += lc[index_to_append]
    keyword_index += 1
print(final_message.replace("x", " "))
