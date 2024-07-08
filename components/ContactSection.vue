<template>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.12.1/css/all.min.css" integrity="sha256-mmgLkCYLUQbXn0B1SRqzHar6dCnv9oZFPEC1g1cwlkk=" crossorigin="anonymous" />
<section class="contact">
    <div class="container">
        <div class="row">
            <div class="col-lg-6">
                <div class="section-title">
                    <h2>Get In Touch</h2>
                </div>
            </div>
        </div>
        <div class="row flex-row-reverse">
            <div class="col-md-7 col-lg-8 m-15px-tb">
                <div class="contact-form">
                     <form action="/" method="post" class="contactform contact_form" id="contact_form">
                        <div class="returnmessage valid-feedback p-15px-b" data-success="Your message has been received, We will contact you soon."></div>
                        <div class="empty_notice invalid-feedback p-15px-b"><span>Please Fill Required Fields</span></div>
                        <div class="row">
                            <div class="col-md-6">
                                <div class="form-group">
                                    <input id="name" type="text" placeholder="Full Name" class="form-control"> 
                                </div>
                            </div>
                            <div class="col-md-6">
                                <div class="form-group">
                                    <input id="email" type="text" placeholder="Email Address" class="form-control">  
                                </div>
                            </div>
                            <div class="col-12">
                                <div class="form-group">
                                    <input id="subject" type="text" placeholder="Subject" class="form-control"> 
                                </div>
                            </div>
                            <div class="col-md-12">
                                <div class="form-group">
                                    <textarea id="message" placeholder="Message" class="form-control" rows="3"></textarea> 
                                </div>
                            </div>
                            <button class="btn btn-primary"> contact us </button>
                        </div>
                    </form>
                </div>
            </div>
            <div class="col-md-5 col-lg-4 m-15px-tb">
                <div class="contact-name">
                    <h5>Mail</h5>
                    <p>faizdaffakurnia@gmail.com</p>
                </div>
                <div class="contact-name">
                    <h5>Address</h5>
                    <p>Condongcatur, Sleman, <br>Daerah Istimewa Yogyakarta</p>
                </div>
                <div class="contact-name">
                    <h5>Phone</h5>
                    <p>0858-0275-4890</p>
                </div>
            </div>
        </div>
    </div>
</section>
 
 </template>
 
 <script>
 export default {
   data() {
     return {
       name: '',
       email: '',
       message: '',
       success: false,
       error: false,
     };
   },
   methods: {
     async sendMessage() {
       try {
         // Kirimkan data form ke backend Anda di sini
         // Contoh menggunakan Axios
         const response = await axios.post('/api/contact', {
           name: this.name,
           email: this.email,
           message: this.message,
         });
 
         if (response.status === 200) {
           this.success = true;
           this.error = false;
         } else {
           this.error = true;
           this.success = false;
         }
       } catch (error) {
         this.error = true;
         this.success = false;
         console.error(error);
       } finally {
         // Reset form setelah terkirim
         this.name = '';
         this.email = '';
         this.message = '';
       }
     },
   },
 };
 </script>
 
 <style>

body{
    color: #6F8BA4;
    margin-top:20px;}
    
.contact {
  margin-top: 60px;
    padding: 100px 0;
    position: relative;
    background-image: url(https://images.unsplash.com/photo-1628882185379-0dd168dfd07a?q=80&w=2008&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D);
    height: 100vh;
}
/* Contact Us
---------------------*/
.contact-name {
  margin-bottom: 30px;
}
.contact-name h5 {
  font-size: 22px;
  color: #000000;
  margin-bottom: 5px;
  font-weight: 600;
}
.contact-name p {
  font-size: 18px;
  margin: 0;
}

.social-share a {
  width: 40px;
  height: 40px;
  line-height: 40px;
  border-radius: 50%;
  color: #ffffff;
  text-align: center;
  margin-right: 10px;
}


.contact-form .form-control {
  border: none;
  border-bottom: 1px solid #000000;
  background: transparent;
  border-radius: 0;
  padding-left: 0;
  box-shadow: none !important;
}
.contact-form .form-control:focus {
  border-bottom: 1px solid #fc5356;
}
.contact-form .form-control.invalid {
  border-bottom: 1px solid #ff0000;
}
.contact-form .send {
  margin-top: 20px;
}
@media (max-width: 767px) {
  .contact-form .send {
    margin-bottom: 20px;
  }
}

.section-title h2 {
    font-weight: 700;
    font-size: 45px;
    margin: 0 0 15px;
    border-left: 5px solid #000000;
    padding-left: 15px;
}
.section-title {
    padding-bottom: 45px;
}

 </style>
 
