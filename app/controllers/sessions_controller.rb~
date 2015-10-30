class SessionsController < ApplicationController
  def new

  end

  def create
    #render 'new'
    user = User.find_by(email: params[:session][:email].downcase)
    if user && user.athenticate(params[:Session][:password])
      log_in user
      redirect_to user
      # log the user in and show show page
    else
      flash.now[:danger] = 'Invalid e-mail/password compination' # it's not quite right
      render 'new'
    end
  end

  def destroy
    
  end
end
