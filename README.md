# Repo-Nico

def anagrams(filename='poezie.txt'):
    with open(filename) as f:
        for word in f:
            yield word.rstrip()

def find_anagrams(source):
    for word in source:
        key = "".join(sorted(word))
        d[key].append(word)
    return d

def print_anagrams(word_source):
    d = get_anagrams(word_source)
    for key, anagrams in d.iteritems():
        if len(anagrams) > 1:
            print(key, anagrams)

word_source = load_words()
print_anagrams(word_source)

if __name__ == '__main__':
    anagrams = find_anagrams(words)
    print ("Anagram count:", len(anagrams), "\n")
