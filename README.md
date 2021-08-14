Observable/Subject

UserService > activatedEmitter = new Subject<boolean>();
  
this.userService.activatedEmitter.next(true);
  
 app.component.ts
  
    ngOnInit() {
    this.activatedSub = this.userService.activatedEmitter.subscribe(didActivate => {
      this.activateUser = didActivate;
    })
  }
