
<script>
    
    
        import b1 from '../assets/desktop-image-hero-1.jpg'
        import b2 from '../assets/desktop-image-hero-2.jpg'
        import b3 from '../assets/desktop-image-hero-3.jpg'
    
        let list =[b1,b2,b3];
        let active=b1;
    
        const next=()=>{
            let n =list.length - 1;
            // console.log(n);
            for (let index = 0; index < list.length; index++) {
                if(n === index){
                    // console.log('yes');
                    active=list[0];
                    break;   
                 }
                
                if(list[index] === active){
                index +=1;
                // console.log(index);
                active=list[index];
                break;
                
                }
             }
        }
        const prev=()=>{
            
            for (let index = 0; index < list.length; index++) {
                let n =list.length -1;
                if(list[0] ===active){
               active=list[n];
                break;   
                }
                if(list[index] ===active){
                index -=1;
                
               active=list[index];
                break;
                
                }
                
             }
         
        }
    
        import a1 from '../assets/image-about-dark.jpg'
        import a2 from '../assets/image-about-light.jpg'
        // import b1 from '../assets/desktop-image-hero-1.jpg'
    </script>
    
    
    <div class="flex w-full ">
        <nav class="absolute z-20 w-full flex ">
           <ul class="flex w-1/3 justify-between m-10">
               <li>
                  <h1 class="text-xl font-semibold text-white">Home</h1>
                </li>
               <li class="text-white">shop</li>
               <li class="text-white">about</li>
               <li class="text-white">contact</li>
               <li class="text-white">help</li>
           </ul>
        </nav>
       
        <div class="w-full relative  bg-no-repeat " style="background-image: url('{active}')">
            <div class="absolute h-20 bg-black w-40 bottom-0 -right-10  flex justify-start">
              <button on:click={prev}  class="flex justify-center items-center w-20 h-full bg-black hover:bg-gray-800 text-white focus:outline-none">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                </svg>
            </button>
              <button on:click={next}  class="flex justify-center items-center w-20 h-full bg-black hover:bg-gray-800 text-white focus:outline-none">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                  </svg>
              </button>
            </div>
        </div>
    
        <div class="flex justify-crenter items-center w-1/2 h-1/2">
            <div class="space-y-4 h-full w-full my-28 mx-10 ">
                <h1 class="text-4xl font-semibold mt-10 ">Discover innovative ways to decorate </h1>
                <p class="text-gray-400">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Autem ut tempore laborum reprehenderit labore deleniti? Delectus vel cum fugit veniam. Laborum sint at quidem aspernatur ullam quos inventore ex saepe.</p>
                <h2 class="text-xl text-gray-400 flex uppercase tracking-widest font-light">shop now 
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-9 w-9 mx-4 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                  </svg>
                </h2>
    
               
            </div>
            
        </div>
    </div>
    <div class="grid grid-cols-3 w-full h-72 space-x-10">
            <div class="w-full bg-no-repeat " style="background-image: url('{a1}')"></div>
            <div class="w-full px-6 py-20 space-y-4  ">
              
                    <h1 class="font-semibold uppercase text-lg tracking-widest">about our furniture</h1>
                    <p class="text-gray-400">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque eum fugit enim libero temporibus incidunt veniam, mollitia fuga quaerat doloribus architecto aspernatur nulla dolorum odit. Vel corporis ea doloremque quis?</p>
            </div>
            <div  class="w-full bg-no-repeat "style="background-image: url('{a2}')"></div>
    </div>
    
    