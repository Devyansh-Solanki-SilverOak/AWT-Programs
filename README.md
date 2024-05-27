## Code for calling our functions

```
try{
    if(simplyInsurance && typeof simplyInsurance !== "undefined" )
        simplyInsurance.loadApp();
}catch(e){
    console.log(e);
}
```

## Title

```
<div class="si-widget"></div>
<img width="1" height="1" alt="shipping protection"
style="width: 1px; height: 1px;" onLoad="simplyInsurance.loadApp();"
src="data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==" />
```

## Title

```
document.body.dispatchEvent(new CustomEvent("cart:refresh"));
document.body.dispatchEvent(new CustomEvent("added.ajaxProduct"));
theme.jQuery("body").trigger("added.ajaxProduct");
```

## Title

```
const search = what => simplyInsurance.insurancePlan.planArray.find(element => element.variant_id == what);
window.SLIDECART_REMOVED_FROM_CART = function({ id }) {
    // Fires whenever an item is removed from cart
    console.log(id);
    const found = search(id);
    if (found) {
        simplyInsurance.toggleUncheck();
    } else {
        console.log('No result found');
    }
    // debugger;
}
```

## Title

```
  getSectionInnerHTML= function(html, selector = '.shopify-section') {
    return new DOMParser()
      .parseFromString(html, 'text/html')
      .querySelector(selector).innerHTML;
  }

  getSectionsToRender= function() {
    return [
      {
        id: 'cart-drawer',
        selector: '#CartDrawer'
      },
      {
        id: 'cart-icon-bubble'
      }
    ];
  }

  getSectionDOM= function(html, selector = '.shopify-section') {
    return new DOMParser()
      .parseFromString(html, 'text/html')
      .querySelector(selector);
  }

  renderContents = function(parsedState) {
    this.getSectionsToRender().forEach((section => {
      const sectionElement = section.selector ? document.querySelector(section.selector) : document.getElementById(section.id);
      sectionElement.innerHTML = this.getSectionInnerHTML(parsedState[section.id], section.selector);
    }));
  }

  fetch(window.Shopify.routes.root + "?sections=cart-drawer,cart-icon-bubble")
    .then(res => res.json())
    .then((state) => {
      console.log(state['cart-drawer'])
      renderContents(state)
    });
```

## Title

```
document.documentElement.dispatchEvent(new CustomEvent('cart:refresh', {
    bubbles: true    // same code for prestige theme
}));

// blockshop theme
theme.cart.updateAllHtml();
theme.cart.updateTotals();

// impulse theme
document.dispatchEvent(new CustomEvent('cart:build'));
```

## Title

Shipping Protection from Damage, Loss & Theft for ##plan_price 
```
<button type="button" class="btnCstm tooltipCstm">
    <svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M7.5 0C3.36433 0 0 3.36433 0 7.5C0 11.6357 3.36433 15 7.5 15C11.6357 15 15 11.6357 15 7.5C15 3.36433 11.6357 0 7.5 0ZM7.5 11.875C7.15496 11.875 6.87504 11.595 6.87504 11.25C6.87504 10.905 7.15496 10.625 7.5 10.625C7.84504 10.625 8.12496 10.905 8.12496 11.25C8.12496 11.595 7.84504 11.875 7.5 11.875ZM8.48934 7.90123C8.26813 8.00308 8.12496 8.22624 8.12496 8.46943V8.75004C8.12496 9.09496 7.84561 9.375 7.5 9.375C7.15439 9.375 6.87504 9.09496 6.87504 8.75004V8.46943C6.87504 7.73998 7.30373 7.0713 7.96566 6.76563C8.60252 6.47255 9.06246 5.69435 9.06246 5.31246C9.06246 4.45129 8.36185 3.75 7.5 3.75C6.63815 3.75 5.93754 4.45129 5.93754 5.31246C5.93754 5.6575 5.65807 5.93754 5.31246 5.93754C4.96685 5.93754 4.6875 5.6575 4.6875 5.31246C4.6875 3.7619 5.94933 2.49996 7.5 2.49996C9.05067 2.49996 10.3125 3.7619 10.3125 5.31246C10.3125 6.15692 9.57996 7.39815 8.48934 7.90123Z" fill="#212B36"></path>
    </svg>
    <span class="toolltiptextCstm">
        Get peace of mind with Shipping Protection in the event your delivery is damaged, stolen, or lost during transit.
    </span>
</button>

<style>
.tooltipCstm {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted #000;
}

.tooltipCstm .toolltiptextCstm {
  visibility: hidden;
  width: 120px;
  background-color: #000;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 5px 0;
  position: absolute;
  z-index: 1;
  bottom: 100%;
  left: 50%;
  margin-left: -60px;
}

.tooltipCstm:hover .toolltiptextCstm {
  visibility: visible;
}

.tooltipCstm .toolltiptextCstm {
  font-size: 12px;
  text-align: left;
  width: 200px !important;
  height: auto;
  display: inline-block;
  line-height: 14px;
  min-width: 100px;
  word-break: break-word;
  white-space: normal;
  margin-bottom: 5px;
  padding-left: 10px;
  padding-right: 10px;
  border-radius: 10px;
}

.btnCstm.tooltipCstm {
    width: auto;
    background: none;
    border: none;
    display:inline-block;
}
</style>
```
