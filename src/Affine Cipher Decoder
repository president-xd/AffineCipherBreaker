def affine_cipher_decrypt(ciphertext, a, b):
    """Decrypts the ciphertext using the Affine cipher with keys a and b."""
    try:
        def mod_inverse(x, mod):
            for i in range(mod):
                if (x * i) % mod == 1:
                    return i
            return None
        
        decrypted_text = []
        mod_inv_a = mod_inverse(a, 26)
        
        if mod_inv_a is None:
            raise ValueError("No modular inverse exists for the given 'a' value in the Affine Cipher.")
        
        for char in ciphertext:
            if char.isalpha():
                base = ord('A') if char.isupper() else ord('a')
                decrypted_char = chr((mod_inv_a * (ord(char) - base - b)) % 26 + base)
                decrypted_text.append(decrypted_char)
            else:
                decrypted_text.append(char)
        
        return ''.join(decrypted_text)
    except Exception as ex:
        print(EXCEPTION_MESSAGE, ex)
        
print(affine_cipher_decrypt("RCLLA Zrcp wu uaqczrwvm vco", 5, 8))        
        
