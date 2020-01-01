const obj = {
    value: 'abc',
    createArrowFn: function() {
        return () => console.log(this);
    }
};

const arrowFn = obj.createArrowFn();
arrowFn(); // ?

---

{ value: 'abc', createArrowFn: ƒ }