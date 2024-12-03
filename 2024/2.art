reports: chop to [:block[:integer]] read.lines ./"2.txt" 

safe?: $[b][
    sign: b\0 - b\1
    loop 0..sub size b 2 'i [
        diff: b\[i] - b\[i+1]
        if (1 > sign * diff) ∨ ¬ <=> abs diff 1 3 -> return false
    ] 
    true
]

without1: $[b][
    map.with:'i b => [remove.index b i]
]

;part 1
print enumerate reports => safe?

;part 2
print enumerate reports => [
    some? without1 & => safe?
]
