#core/mathematicalphysics #core/machinelearning

![[one-hot-encoding.jpg]]

One-hot encoding is a **method used to convert categorical data into a binary, numeric format** that machine learning algorithms can easily process.

## How It Works

1. **Identify Unique Categories**
   - Determine all unique categories in your dataset.
   - Example: For a 'colour' feature with categories 'red', 'blue', and 'green', these are your unique categories.

2. **Create Binary Vectors**
   - For each unique category, create a new binary vector.
   - The length of the vector equals the number of unique categories.

3. **Encoding Process**
   - Place a '1' in the vector position corresponding to the category it represents.
   - Fill other positions with '0's.

## Example

Given categories: 'red', 'blue', and 'green'.

- **Red:** `[1, 0, 0]`
- **Blue:** `[0, 1, 0]`
- **Green:** `[0, 0, 1]`

## Benefits

- **Numeric Representation:** Converts categorical data to a numeric form, making it easier for machine learning algorithms to process.
- **No Ordinal Assumption:** This does not imply any ordinal relationship between categories, unlike numeric encoding.
