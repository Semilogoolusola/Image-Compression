function [code, dict] = huffman_encode(vector)
% huffman_encode performs huffman ecncoding on a given array.
%
%   Input:
%      vector: 1D run length encoded array.
%
%   Output: 
%      code: the huffman coded array.
%      dict: dictionary of the symbols and their pobabilites
    
    symbols = unique(vector);
    occurences = zeros(size(symbols));
    
    for i = 1 : length(vector)
        occurences(symbols == vector(i)) = occurences(symbols == vector(i)) + 1;
    end
    
    %Calculate the probabilities
    probabilities = occurences/sum(occurences);
    dict = huffmandict(symbols, probabilities);
    code = huffmanenco(vector,dict);
end
