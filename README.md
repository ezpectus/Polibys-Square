



**Code Explanation:**

**1. `Method` Enum:**

* This defines two different methods for encryption: `Method1` and `Method2`. These methods change how the coordinates of the characters are used during encryption and decryption.

**2. `PolybiusSquare` Class:**

* **Fields:**
    * `square`: A 2D character array representing the Polybius Square.
    * `alphabet`: The characters used to fill the square. Defaults to uppercase letters and a space.
    * `encryptMethod`: The encryption method to use.
* **Constructor:**
    * Initializes the `alphabet` and `encryptMethod`.
* **`GetSquare(string key)` Method:**
    * Creates the Polybius Square based on a given `key`.
    * Removes characters from the `alphabet` that are in the `key`.
    * Adds the `key` to the beginning of the `alphabet` and extra characters to the end.
    * Calculates the size of the square.
    * Fills the `square` with characters from the modified `alphabet`.
* **`FindSymbol(char[,] symbolsTable, char symbol, out int column, out int row)` Method:**
    * Finds the coordinates (row and column) of a given `symbol` in the `symbolsTable`.
    * Returns `true` if the symbol is found, `false` otherwise.
* **`PolibiusEncrypt(string text, string password)` Method:**
    * Encrypts the input `text` using the Polybius Square and the given `password`.
    * Uses the `encryptMethod` to determine how to encrypt.
    * **`Method1`:** Replaces each character with the character below it in the square.
    * **`Method2`:** Stores the coordinates of each character and then uses them to encrypt.
* **`PolibiusDecrypt(string text, string password)` Method:**
    * Decrypts the input `text` using the Polybius Square and the given `password`.
    * Uses the `encryptMethod` to determine how to decrypt.
    * **`Method1`:** Replaces each character with the character above it in the square.
    * **`Method2`:** Reverses the coordinate swapping from `Method2` encryption.

**3. `Program` Class:**

* **`Main(string[] args)` Method:**
    * Creates a `PolybiusSquare` object.
    * Prompts the user to enter the message and password.
    * Encrypts the message using `PolibiusEncrypt`.
    * Decrypts the encrypted message using `PolibiusDecrypt`.
    * Prints the encrypted and decrypted messages to the console.

**In Simple Terms:**

This program takes a message and a password, and it uses a special grid (the Polybius Square) to turn the message into a secret code. It can also turn the secret code back into the original message. There are two different ways it can do this, which are called `Method1` and `Method2`.

**Key Concepts:**

* **Polybius Square:** A grid used for simple substitution ciphers.
* **Encryption:** Turning a message into a secret code.
* **Decryption:** Turning a secret code back into a message.
* **2D Arrays:** Used to represent the Polybius Square.
* **Enums:** Used to define the encryption methods.
* **String Manipulation:** Used to create and modify the alphabet and the encrypted/decrypted text.


