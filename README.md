# Handling_Events

# Song Cart 

Yeh ek simple React application hai jo ek song ki list dikhata hai, har song ke saath uska description aur ek "Download now" button. Jab aap button pe click karte ho, ek alert aata hai.

## Code Explanation

### `SongCart.js`

1. **Importing React**:
    ```javascript
    import React from 'react'
    ```
    Yeh line React ko import kar rahi hai taaki hum React component bana sakein.

2. **SongCart Function**:
    ```javascript
    function SongCart() {
    ```
    `SongCart` naam ka ek functional component bana rahe hain.

3. **Data Array**:
    ```javascript
    const data = [
        {
            name: "Pal Pal Dil Ke Pass",
            description: "A romantic song from the movie 'Pal Pal Dil Ke Pass', expressing deep love and emotions with soothing music."
        },
        {
            name: "Tum Hi Ho",
            description: "A heart-touching love song from the movie 'Aashiqui 2', depicting eternal  and devotion this feels good and best."
        },
        {
            name: "Shape of You",
            description: "A catchy, upbeat song by Ed Sheeran with a tropical rhythm that became a global hit and a dance floor favorite."
        },
        {
            name: "Hasi",
            description: "A beautiful romantic ballad from the movie 'Hamari Adhuri Kahani', filled with heartfelt lyrics and soulful music."
        }
    ]
    ```
    Yeh ek `data` naam ka array hai jisme kuch songs ke naam aur unke descriptions hain. Hum inhe render karenge.

4. **Handle Click for Download**:
    ```javascript
    const handleClickDownload = ()=>{alert("Download will start in 3s.....")}
    ```
    Yeh ek function `handleClickDownload` define kar raha hai jo jab "Download now" button click hota hai, tab ek alert show karega.

5. **Returning JSX (Rendering Data)**:
    ```javascript
    return (
        <div>
            <div className='w-full h-screen bg-zinc-300 flex flex-col justify-center items-center gap-5 ' >
                {data.map((item, index)=>(
                    <div className='w-[500px] px-3 py-2  bg-zinc-100  rounded-md' >
                        <h3 className='text-black font-semibold mb-0.5' >{item.name}</h3>
                        <p className='font-xs text-xs' >{item.description}</p>
                        <button onClick={handleClickDownload} className='bg-blue-500 text-white px-2 py-1 mt-2 text-xs rounded' >Download now</button>
                    </div>
                ))}
            </div>
        </div>
    )
    ```
    Yeh code JSX mein likha gaya hai jo React ko bata raha hai ki kaise UI render hoga:
    - Sabse pehle, ek `div` create ho raha hai jo screen ko cover karega.
    - Phir, `data.map()` ka use kar ke hum har song ko render kar rahe hain.
    - Har song ke liye, ek card ban raha hai jisme song ka `name` aur `description` dikh raha hai.
    - Har card ke niche ek "Download now" button bhi hai jo `handleClickDownload` function ko call karega.

6. **Exporting SongCart**:
    ```javascript
    export default SongCart
    ```
    Yeh line `SongCart` component ko export kar rahi hai taaki hum isse kahin bhi import karke use kar sakein.

---

## Conclusion

Yeh React app ek simple song list display karta hai. Aap "Download now" button pe click karte ho to ek alert show hota hai. Aap is code ko customize kar ke aur songs add kar sakte ho.

