<template>
    <div class="container">
      <div class="d-flex justify-content-center">
        <div class="square d-flex justify-content-center align-items-center">
          <i class="fa-solid fa-medal fa-xl" style="color: #ffffff;"></i>
        </div>
      </div>
      <div class="text-center py-3">
        <h3>Special Packs</h3>
        <p>Select pricing plan to get more</p>
      </div>
      <div class="section-cards d-flex justify-content-between w-100">
        <div class="packs text-center">
          <div class="pack-content">
            <div class="pack-top py-3">
              <div class="icon py-2"><i class="fa-regular fa-handshake fa-xl" style="color: #ffffff;"></i></div>
              <div class="top-text py-2">
                <h6>Basic</h6>
                <p>Learn to ride a bike from the professional</p>
              </div>
            </div>
            <div class="pack-bottom py-4">
              <ul class="d-flex flex-column justify-content-center">
                <li class="text-center p-1">✓ Phone Mountaineer bike training</li>
                <li class="text-center p-1">✓ Remote Excellent bike service</li>
                <li class="text-center p-1">✓ Onsite Safe cycling training</li>
                <li class="text-center p-1">✗ Saafety helmet on bike</li>
                <li class="text-center p-1">✗ Free bikes for children</li>
              </ul>
            </div>
            <div class="pack-info">
                <div>
                    <h5>BASIC</h5>
                    <h4>$1800</h4>
                </div>
                <button type="button" class="btn-form my-2">Send Request!</button>
            </div>
          </div>
        </div>
        <div class="packs text-center">
          <div class="pack-content">
            <div class="pack-top py-3">
              <div class="icon py-2"><i class="fa-solid fa-helmet-safety fa-xl" style="color: #ffffff;"></i></div>
              <div class="top-text py-2">
                <h6>Standard</h6>
                <p>Learn to ride a bike from the professional</p>
              </div>
            </div>
            <div class="pack-bottom py-4">
              <ul class="d-flex flex-column justify-content-center">
                <li class="text-center p-1">✓ Phone Mountaineer bike training</li>
                <li class="text-center p-1">✓ Remote Excellent bike service</li>
                <li class="text-center p-1">✓ Onsite Safe cycling training</li>
                <li class="text-center p-1">✗ Saafety helmet on bike</li>
                <li class="text-center p-1">✗ Free bikes for children</li>
              </ul>
            </div>
            <div class="pack-info">
                <div>
                    <h5>STANDARD</h5>
                    <h4>$2500</h4>
                </div>
                <button type="button" class="btn-form my-2">Send Request!</button>
            </div>
          </div>
        </div>
        <div class="packs text-center">
          <div class="pack-content">
            <div class="pack-top py-3">
              <div class="icon py-2"><img src="/images/Screenshot 2023-11-23 122012.png" alt="img"></div>
              <div class="top-text py-2">
                <h6>Premium</h6>
                <p>Learn to ride a bike from the professional</p>
              </div>
            </div>
            <div class="pack-bottom py-4">
              <ul class="d-flex flex-column justify-content-center">
                <li class="text-center p-1">✓ Phone Mountaineer bike training</li>
                <li class="text-center p-1">✓ Remote Excellent bike service</li>
                <li class="text-center p-1">✓ Onsite Safe cycling training</li>
                <li class="text-center p-1">✗ Saafety helmet on bike</li>
                <li class="text-center p-1">✗ Free bikes for children</li>
              </ul>
            </div>
            <div class="pack-info">
                <div>
                    <h5>PREMIUM</h5>
                    <h4>$5000</h4>
                </div>
                <button type="button" class="btn-form my-2">Send Request!</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Section6',
    data() {
        return {};
    },
  };
  </script>
  
  <style lang="scss" scoped>

.square{
    width: 90px;
    height: 90px;
    background-color: black;
    color: white;
    font-size: 1.5em;
}
.packs {
    position: relative;
    width: calc((100% / 3) - 40px);
    box-shadow: 1px 1px 10px 1px black;
    transition: transform 1s ease;
    height: 420px;
  
    &:hover {
      transform: rotateY(-180deg);
      background-color: black;
    } 
}
  
    .pack-info {
        display: none;
        background-color: black;
        color: white;
        border-radius: 5px;
        padding: 10px;
        transition: display 1s ease;
        height: 420px;
       .btn-form{
        border: 1px solid white;
        padding: 20px 30px 20px 30px;
       }
      }
    .packs:hover .pack-info{
        display: block;
        transition: display 2s ease-in-out;
        transform: rotateY(-180deg);
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        align-content: center;
        h4{
            font-size: 2.3em;
        }
        h5{
            font-size: 1.2em;
        }
    }
    .packs:hover .pack-top,.packs:hover .pack-bottom{
        display: none;
        transition: display 2s ease-in-out;

    }
  
    .pack-content {
      position: relative;
      width: 100%;
      height: 100%;
    }
      .pack-top {
        background-color: black;
        color: white;
        border-radius: 5px 5px 0 0;
  
        .icon {
          font-size: 40px;
        }
  
        h6 {
          font-weight: 600;
        }
      }
  
  
        .pack-bottom {
            border-radius: 0 0 5px 5px;

            ul {
            list-style: none;
                li {
                    border-bottom: 1px solid #f5f5f5;
                }
            }
        }
        img{
            width: 80px;
            margin-bottom: -20px;
        }
    
  </style>
  