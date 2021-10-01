# Validation Library

It is a client side validation script and will be useful for form validations with some basic validations. This is built with jquery version 3.2.1 at the time of creation. You can use this plugin to your projects this will automatically take jquery plugin if not available in your project.

**Syntax**

```javascript
var obj=new formValidations();
var validations={
      formID:'validateForm', /* Id of the validation form */
      fields: {
        'name of the tag':{
          validators:{
            /* To validate the input if empty */
            notEmpty:{
              message:'Validation message if field empty'
            },
            /* To validate the input with email address format */
            emailAddress: {
                message: 'The input is not a valid email address'
            },
            /* To restrict the length of the input string */
            strLen:{
                min:5,
                max:10,
                message:'The password must have 5 to 10 characters'
             },
             /* To restrict the strength of the password */
             strength:{
                severity:'medium',
                message:'Minimum one alphabet and one number.'
                /*severity:'high',
                message:'Minimum one upper case, one lower case, one number.'*/
                /*severity:'strict',
                message:'Minimum one upper case, one lower case, one number and one special character.'*/
              },
              /* To compare the text between two input fields and restrict if not matched */
              compare:{
                input:'input-name', /* Name of the input field to be compare  */
                message:'Text not matched'
              },
              /* To restrict the input field with number only */
              numberOnly:{
                message:'Enter number only'
              },
              /* To restrict the size of the file input  */
              fileSize:{
                max:1000000, /* in Bytes */
                message:'File size should be less than 1 mb'
              },
               /* To restrict the extensions of the file input  */
              extensions:{
                allowed:['jpg','jpeg','png','gif','bmp'],
                message:'Only images are allowed'	
              },
              /* To restrict the resolutions of the file input if it is image  */
              resolutions:{
                width:645,
                height:645,
                message:'Image resoultion should be 645 and 645'
              }
          }
        }
      }
}
obj.validateForm(validations,function(response){
});
```

**You can also use some predefined class to restrict your input fields on key press**

- numeric-only
- alphabet-only


# **Demo link is available**

https://demolinc.com/validation/

